# Il2cppListHook
A simple System.Collections.Generic.List&lt;T> hook for il2cpp x64 builded apps. Creates a "fake" .net-list and swap it data with original's list data

*How to use:*
- Create MimicList<T> obj and add data to it (T must be ptr if original list stores ref for some managed class);
- Get the pointer to a .net list;
- Call set_list_data(uintptr_t) and pass pointer to .net list;
- Call swap() to swap fake list data with original. You still can change MimicList<T> after swap, all data will be update in original .net list;
	
Note that restore() must be called before original .net list will be deleted!