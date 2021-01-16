---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354021"
---
# <span data-ttu-id="a3b09-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3b09-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="a3b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3b09-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b09-103">Azure RBAC에서 사용자 지정 역할을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="a3b09-104">수정된 역할 정의를 JSON 파일 또는 PSRoleDefinition으로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="a3b09-105">먼저 Get-AzRoleDefinition 명령을 사용하여 수정하고자 하는 사용자 지정 역할을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="a3b09-106">그런 다음 변경할 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="a3b09-107">마지막으로 이 명령을 사용하여 역할 정의를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="a3b09-108">구문</span><span class="sxs-lookup"><span data-stu-id="a3b09-108">SYNTAX</span></span>

### <span data-ttu-id="a3b09-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b09-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3b09-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b09-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3b09-111">설명</span><span class="sxs-lookup"><span data-stu-id="a3b09-111">DESCRIPTION</span></span>
<span data-ttu-id="a3b09-112">Set-AzRoleDefinition cmdlet은 Azure Role-Based Access Control에서 기존 사용자 지정 역할을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="a3b09-113">JSON 파일 또는 PSRoleDefinition 개체로 명령에 대한 입력으로 업데이트된 역할 정의를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="a3b09-114">업데이트된 사용자 지정 역할에 대한 역할 정의는 업데이트되지 않은 경우에도 ID 및 역할의 기타 모든 필수 속성(DisplayName, Description, Actions, AssignableScopes)을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="a3b09-115">NotActions, DataActions, NotDataActions는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="a3b09-116">다음은 Set-AzRoleDefinition { "Id"에 대한 업데이트된 역할 정의 json 샘플입니다. "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "업데이트된 역할", "설명": "모든 리소스를 모니터링하고 가상 머신을 시작 및 다시 시작할 수 있습니다.", "Actions": \[ *"/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "/write"* \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxx-xxxx-x-x-x" \] }</span><span class="sxs-lookup"><span data-stu-id="a3b09-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="a3b09-117">예제</span><span class="sxs-lookup"><span data-stu-id="a3b09-117">EXAMPLES</span></span>

### <span data-ttu-id="a3b09-118">예제 1: PSRoleDefinitionObject를 사용하여 업데이트</span><span class="sxs-lookup"><span data-stu-id="a3b09-118">Example 1: Update using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="a3b09-119">예제 2: JSON 파일을 사용하여 만들기</span><span class="sxs-lookup"><span data-stu-id="a3b09-119">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="a3b09-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3b09-120">PARAMETERS</span></span>

### <span data-ttu-id="a3b09-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b09-121">-DefaultProfile</span></span>
<span data-ttu-id="a3b09-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a3b09-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3b09-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a3b09-123">-InputFile</span></span>
<span data-ttu-id="a3b09-124">업데이트할 단일 json 역할 정의를 포함하는 파일 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="a3b09-125">JSON에서 업데이트할 속성만 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="a3b09-126">Id 속성은 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-126">Id property is Required.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b09-127">-Role</span><span class="sxs-lookup"><span data-stu-id="a3b09-127">-Role</span></span>
<span data-ttu-id="a3b09-128">업데이트할 역할 정의 개체</span><span class="sxs-lookup"><span data-stu-id="a3b09-128">Role definition object to be updated</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b09-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b09-129">CommonParameters</span></span>
<span data-ttu-id="a3b09-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b09-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b09-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3b09-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b09-132">입력</span><span class="sxs-lookup"><span data-stu-id="a3b09-132">INPUTS</span></span>

### <span data-ttu-id="a3b09-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3b09-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="a3b09-134">출력</span><span class="sxs-lookup"><span data-stu-id="a3b09-134">OUTPUTS</span></span>

### <span data-ttu-id="a3b09-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3b09-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="a3b09-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3b09-136">NOTES</span></span>
<span data-ttu-id="a3b09-137">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="a3b09-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a3b09-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3b09-138">RELATED LINKS</span></span>

[<span data-ttu-id="a3b09-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="a3b09-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="a3b09-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3b09-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="a3b09-141">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3b09-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="a3b09-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a3b09-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)
