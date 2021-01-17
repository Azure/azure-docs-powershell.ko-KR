---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342237"
---
# <span data-ttu-id="b0c1b-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b0c1b-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="b0c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c1b-103">Azure RBAC에서 사용자 지정 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="b0c1b-104">JSON 역할 정의 파일 또는 PSRoleDefinition 개체를 입력으로 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="b0c1b-105">먼저 Get-AzRoleDefinition 명령을 사용하여 기준 역할 정의 개체를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="b0c1b-106">그런 다음, 필요한 경우 해당 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="b0c1b-107">마지막으로, 이 명령을 사용하여 역할 정의를 사용하여 사용자 지정 역할을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="b0c1b-108">구문</span><span class="sxs-lookup"><span data-stu-id="b0c1b-108">SYNTAX</span></span>

### <span data-ttu-id="b0c1b-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c1b-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0c1b-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0c1b-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0c1b-111">설명</span><span class="sxs-lookup"><span data-stu-id="b0c1b-111">DESCRIPTION</span></span>
<span data-ttu-id="b0c1b-112">New-AzRoleDefinition cmdlet은 Azure Role-Based Access Control에서 사용자 지정 역할을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="b0c1b-113">JSON 파일 또는 PSRoleDefinition 개체로 명령에 대한 입력으로 역할 정의를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="b0c1b-114">입력 역할 정의는 반드시 다음 속성을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="b0c1b-115">DisplayName: 사용자 지정 역할의 이름</span><span class="sxs-lookup"><span data-stu-id="b0c1b-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="b0c1b-116">설명: 역할이 부여하는 액세스를 요약하는 역할에 대한 간략한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="b0c1b-117">작업: 사용자 지정 역할이 액세스 권한을 부여하는 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="b0c1b-118">Azure Get-AzProviderOperation 사용하여 Azure RBAC를 사용하여 보호할 수 있는 Azure 리소스 공급자에 대한 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="b0c1b-119">다음은 몇 가지 유효한 작업 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="b0c1b-120">"\*/read"는 모든 Azure 리소스 공급자의 읽기 작업에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="b0c1b-121">"Microsoft.Network/\*/read"는 Azure의 Microsoft.Network 리소스 공급자에서 모든 리소스 종류에 대한 읽기 작업에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="b0c1b-122">"Microsoft.Compute/virtualMachines/\*"는 가상 머신 및 해당 자식 리소스 유형의 모든 작업에 대한 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="b0c1b-123">AssignableScopes: 사용자 지정 역할을 할당에 사용할 수 있는 범위 집합(Azure 구독 또는 리소스 그룹)입니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="b0c1b-124">AssignableScopes를 사용하면 사용자 지정 역할을 필요한 구독 또는 리소스 그룹에서만 할당할 수 있도록 할 수 있으며, 나머지 구독 또는 리소스 그룹에 대한 사용자 환경을 희미하게 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="b0c1b-125">다음은 몇 가지 유효한 할당 가능한 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="b0c1b-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": 역할을 두 구독에서 할당할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="b0c1b-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": 역할을 단일 구독에서 할당할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="b0c1b-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": 역할은 네트워크 리소스 그룹에서만 할당할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="b0c1b-129">입력 역할 정의에는 다음 속성이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="b0c1b-130">NotActions: 사용자 지정 역할에 대한 유효 작업을 결정하기 위해 작업에서 제외해야 하는 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="b0c1b-131">사용자 지정 역할에 대한 액세스 권한을 부여하지 않을 특정 작업이 있는 경우 작업에서 특정 작업이 아닌 모든 작업을 지정하는 대신 NotActions를 사용하여 제외하는 것이 편리합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="b0c1b-132">DataActions: 사용자 지정 역할이 액세스 권한을 부여하는 데이터 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="b0c1b-133">NotDataActions: 사용자 지정 역할에 대한 효과적인 데이터 작업을 결정하기 위해 DataActions에서 제외해야 하는 작업 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="b0c1b-134">사용자 지정 역할에서 액세스 권한을 부여하지 않을 특정 데이터 작업이 있는 경우 작업에서 해당 특정 작업이 아닌 모든 작업을 지정하는 대신 NotDataActions를 사용하여 제외하는 것이 편리합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="b0c1b-135">참고: NotActions에서 작업을 지정하는 역할이 사용자에게 할당되어 있으며 다른 역할이 동일한 작업에 대한 액세스 권한을 부여하는 경우 사용자는 해당 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="b0c1b-136">NotActions는 거부 규칙이 아니며 특정 작업을 제외해야 하는 경우 허용되는 작업 집합을 만드는 편리한 방법일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="b0c1b-137">다음은 입력 { "이름": "업데이트된 역할", "설명": "모든 리소스를 모니터링하고 가상 머신을 시작 및 다시 시작할 수 있습니다", "작업": "/read"로 제공될 수 있는 샘플 json 역할 정의입니다. \[ *"Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "/write"* \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xx-x" \] }</span><span class="sxs-lookup"><span data-stu-id="b0c1b-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="b0c1b-138">예제</span><span class="sxs-lookup"><span data-stu-id="b0c1b-138">EXAMPLES</span></span>

### <span data-ttu-id="b0c1b-139">예제 1: PSRoleDefinitionObject를 사용하여 만들기</span><span class="sxs-lookup"><span data-stu-id="b0c1b-139">Example 1: Create using PSRoleDefinitionObject</span></span>
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

### <span data-ttu-id="b0c1b-140">예제 2: JSON 파일을 사용하여 만들기</span><span class="sxs-lookup"><span data-stu-id="b0c1b-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="b0c1b-141">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0c1b-141">PARAMETERS</span></span>

### <span data-ttu-id="b0c1b-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c1b-142">-DefaultProfile</span></span>
<span data-ttu-id="b0c1b-143">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b0c1b-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0c1b-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b0c1b-144">-InputFile</span></span>
<span data-ttu-id="b0c1b-145">단일 json 역할 정의를 포함하는 파일 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-145">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="b0c1b-146">-Role</span><span class="sxs-lookup"><span data-stu-id="b0c1b-146">-Role</span></span>
<span data-ttu-id="b0c1b-147">역할 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-147">Role definition object.</span></span>

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

### <span data-ttu-id="b0c1b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c1b-148">CommonParameters</span></span>
<span data-ttu-id="b0c1b-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c1b-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b0c1b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c1b-151">입력</span><span class="sxs-lookup"><span data-stu-id="b0c1b-151">INPUTS</span></span>

### <span data-ttu-id="b0c1b-152">없음</span><span class="sxs-lookup"><span data-stu-id="b0c1b-152">None</span></span>

## <span data-ttu-id="b0c1b-153">출력</span><span class="sxs-lookup"><span data-stu-id="b0c1b-153">OUTPUTS</span></span>

### <span data-ttu-id="b0c1b-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b0c1b-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="b0c1b-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0c1b-155">NOTES</span></span>
<span data-ttu-id="b0c1b-156">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="b0c1b-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b0c1b-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0c1b-157">RELATED LINKS</span></span>

[<span data-ttu-id="b0c1b-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b0c1b-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="b0c1b-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b0c1b-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="b0c1b-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b0c1b-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="b0c1b-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b0c1b-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

