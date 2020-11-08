---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204422"
---
# <span data-ttu-id="c6f16-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6f16-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="c6f16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f16-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f16-103">Azure RBAC에서 사용자 지정 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="c6f16-104">JSON 역할 정의 파일 또는 PSRoleDefinition 개체 중 하나를 입력으로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="c6f16-105">먼저 Get-AzRoleDefinition 명령을 사용 하 여 기준 역할 정의 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="c6f16-106">그런 다음 필요에 따라 해당 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="c6f16-107">마지막으로이 명령을 사용 하 여 역할 정의를 사용 하 여 사용자 지정 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="c6f16-108">구문과</span><span class="sxs-lookup"><span data-stu-id="c6f16-108">SYNTAX</span></span>

### <span data-ttu-id="c6f16-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6f16-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6f16-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6f16-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6f16-111">설명은</span><span class="sxs-lookup"><span data-stu-id="c6f16-111">DESCRIPTION</span></span>
<span data-ttu-id="c6f16-112">New-AzRoleDefinition cmdlet은 Azure Role-Based 액세스 제어에서 사용자 지정 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="c6f16-113">역할 정의를 JSON 파일 또는 PSRoleDefinition 개체로 명령에 대 한 입력으로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="c6f16-114">입력 역할 정의에는 다음 속성이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="c6f16-115">DisplayName: 사용자 지정 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="c6f16-116">설명: 역할이 부여 하는 액세스를 요약 하는 역할에 대 한 간략 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="c6f16-117">작업: 사용자 지정 역할이 액세스를 허용 하는 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="c6f16-118">Get-AzProviderOperation를 사용 하 여 Azure RBAC를 사용 하 여 보호할 수 있는 Azure 리소스 공급자에 대 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="c6f16-119">다음은 유효한 작업 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="c6f16-120">"\*/read"는 모든 Azure 리소스 공급자의 읽기 작업에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="c6f16-121">"Microsoft. 네트워크/\*/cread"는 Microsoft의 모든 리소스 종류에 대 한 읽기 작업에 대 한 액세스 권한을 Azure의 네트워크 리소스 공급자에 게 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="c6f16-122">"Microsoft. Compute/virtualMachines/\*"는 가상 컴퓨터 및 해당 자식 리소스 형식의 모든 작업에 대 한 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="c6f16-123">AssignableScopes: 사용자 지정 역할을 할당할 수 있는 범위 (Azure 구독 또는 리소스 그룹) 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="c6f16-124">AssignableScopes를 사용 하면 사용자 지정 역할을 필요로 하는 구독 또는 리소스 그룹 에서만 할당할 수 있으며 나머지 구독 또는 리소스 그룹에 대 한 사용자 환경이 복잡 하지 않게 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="c6f16-125">다음은 몇 가지 유효한 할당 가능한 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="c6f16-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": 두 구독에서 역할을 할당에 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="c6f16-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": 단일 구독에서 역할을 할당에 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="c6f16-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": 네트워크 리소스 그룹 에서만 역할을 할당에 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="c6f16-129">입력 역할 정의에는 다음 속성이 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="c6f16-130">NotActions (작업): 사용자 지정 역할에 대 한 유효 작업을 결정 하기 위해 작업에서 제외 해야 하는 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="c6f16-131">사용자 지정 역할에 대 한 액세스 권한을 부여 하지 않으려는 특정 작업이 있는 경우 작업에서 특정 작업을 제외한 모든 작업을 지정 하는 대신 NotActions를 사용 하 여 제외 하면 편리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="c6f16-132">DataActions: 사용자 지정 역할이 액세스를 허용 하는 데이터 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="c6f16-133">NotDataActions: 사용자 지정 역할에 대 한 유효한 데이터 작업을 결정 하기 위해 DataActions에서 제외할 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="c6f16-134">사용자 지정 역할에 대 한 액세스 권한을 부여 하지 않으려는 특정 데이터 작업이 있는 경우에는 작업에서 특정 작업을 제외한 모든 작업을 지정 하는 대신 NotDataActions를 사용 하 여이 작업을 수행 하는 것이 편리 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="c6f16-135">참고: 사용자에 게 NotActions에서 작업을 지정 하 고 다른 역할에 할당 된 동일한 작업에 대 한 액세스 권한을 부여 하는 역할이 할당 되 면 사용자가 해당 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="c6f16-136">NotActions는 거부 규칙이 아니므로 특정 작업을 제외 해야 할 때 허용 되는 작업 집합을 만드는 간단한 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="c6f16-137">다음은 입력 {"Name": "업데이트 된 역할", "설명": "모든 리소스를 모니터링 하 고 가상 컴퓨터를 시작 하 고 다시 시작할 수 있음", "작업", "ClassicCompute/virtualmachines/다시 시작/실행"을 제공 하는 샘플 json 역할 정의입니다. \[ *Microsoft. ClassicCompute/virtualmachines/start/action " \] ," notactions ": \[ "* /Cwrite " \] ," Dataactions ":" \[ Microsoft 저장소/storageaccounts/blobservices/컨테이너/blob/read " \] ," Notdataaction ": \[ " microsoft. 저장소/storageaccounts/blobservices/컨테이너/blob/write " \] ," AssignableScopes ": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx " \] }</span><span class="sxs-lookup"><span data-stu-id="c6f16-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="c6f16-138">예제의</span><span class="sxs-lookup"><span data-stu-id="c6f16-138">EXAMPLES</span></span>

### <span data-ttu-id="c6f16-139">예제 1: PSRoleDefinitionObject를 사용 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="c6f16-139">Example 1: Create using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### <span data-ttu-id="c6f16-140">예제 2: JSON 파일을 사용 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="c6f16-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="c6f16-141">변수</span><span class="sxs-lookup"><span data-stu-id="c6f16-141">PARAMETERS</span></span>

### <span data-ttu-id="c6f16-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f16-142">-DefaultProfile</span></span>
<span data-ttu-id="c6f16-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c6f16-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f16-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="c6f16-144">-InputFile</span></span>
<span data-ttu-id="c6f16-145">단일 json 역할 정의를 포함 하는 파일 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-145">File name containing a single json role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f16-146">-역할</span><span class="sxs-lookup"><span data-stu-id="c6f16-146">-Role</span></span>
<span data-ttu-id="c6f16-147">역할 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-147">Role definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6f16-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f16-148">CommonParameters</span></span>
<span data-ttu-id="c6f16-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6f16-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f16-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c6f16-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f16-151">입력</span><span class="sxs-lookup"><span data-stu-id="c6f16-151">INPUTS</span></span>

### <span data-ttu-id="c6f16-152">않아야</span><span class="sxs-lookup"><span data-stu-id="c6f16-152">None</span></span>

## <span data-ttu-id="c6f16-153">출력</span><span class="sxs-lookup"><span data-stu-id="c6f16-153">OUTPUTS</span></span>

### <span data-ttu-id="c6f16-154">Microsoft. a. PSRoleDefinition (.Resources.</span><span class="sxs-lookup"><span data-stu-id="c6f16-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="c6f16-155">상속자</span><span class="sxs-lookup"><span data-stu-id="c6f16-155">NOTES</span></span>
<span data-ttu-id="c6f16-156">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="c6f16-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c6f16-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6f16-157">RELATED LINKS</span></span>

[<span data-ttu-id="c6f16-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="c6f16-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="c6f16-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6f16-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="c6f16-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6f16-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="c6f16-161">제거-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c6f16-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

