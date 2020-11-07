---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 6ca98bc3a459fada4c9ec7c48c216571fb038ba4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881713"
---
# <span data-ttu-id="80fd6-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="80fd6-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="80fd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="80fd6-103">Azure RBAC의 사용자 지정 역할을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="80fd6-104">수정 된 역할 정의를 JSON 파일 또는 PSRoleDefinition으로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="80fd6-105">먼저 Get-AzureRmRoleDefinition 명령을 사용 하 여 수정할 사용자 지정 역할을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="80fd6-106">그런 다음 변경할 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="80fd6-107">마지막으로,이 명령을 사용 하 여 역할 정의를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80fd6-108">구문과</span><span class="sxs-lookup"><span data-stu-id="80fd6-108">SYNTAX</span></span>

### <span data-ttu-id="80fd6-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="80fd6-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80fd6-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="80fd6-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80fd6-111">설명은</span><span class="sxs-lookup"><span data-stu-id="80fd6-111">DESCRIPTION</span></span>
<span data-ttu-id="80fd6-112">Set-AzureRmRoleDefinition cmdlet은 Azure Role-Based Access Control의 기존 사용자 지정 역할을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="80fd6-113">업데이트 된 역할 정의를 JSON 파일 또는 PSRoleDefinition 개체로 명령에 대 한 입력으로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="80fd6-114">업데이트 된 사용자 지정 역할에 대 한 역할 정의에는 이름, 설명, 동작, AssignableScopes 업데이트 되지 않은 경우에도 해당 역할의 Id 및 기타 모든 필수 속성이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="80fd6-115">NotActions, DataActions, NotDataActions는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="80fd6-116">다음은 Set-AzureRmRoleDefinition {"Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "업데이트 된 역할", "Description": "모든 리소스를 모니터링 하 고 가상 컴퓨터를 시작 하 고 다시 시작할 수 있습니다.", "작업", " \[ *Microsoft ClassicCompute/virtualmachines/다시 시작/작업", "에 대 한 예제 업데이트 역할 정의 json입니다. Microsoft. ClassicCompute/virtualmachines/start/action" \] , "notactions": \[ "* /Cwrite", "dataactions": " \] \[ Microsoft 저장소/storageaccounts/blobservices/컨테이너/blob/read" \] , "Notdataaction": \[ "microsoft. 저장소/storageaccounts/blobservices/컨테이너/blob/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="80fd6-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="80fd6-117">예제의</span><span class="sxs-lookup"><span data-stu-id="80fd6-117">EXAMPLES</span></span>

### <span data-ttu-id="80fd6-118">PSRoleDefinitionObject를 사용 하 여 업데이트</span><span class="sxs-lookup"><span data-stu-id="80fd6-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="80fd6-119">JSON 파일을 사용 하 여 만들기</span><span class="sxs-lookup"><span data-stu-id="80fd6-119">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="80fd6-120">변수</span><span class="sxs-lookup"><span data-stu-id="80fd6-120">PARAMETERS</span></span>

### <span data-ttu-id="80fd6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80fd6-121">-DefaultProfile</span></span>
<span data-ttu-id="80fd6-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="80fd6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80fd6-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="80fd6-123">-InputFile</span></span>
<span data-ttu-id="80fd6-124">업데이트 될 단일 json 역할 정의가 포함 된 파일 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="80fd6-125">JSON에서 업데이트 되는 속성만 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="80fd6-126">Id 속성이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-126">Id property is Required.</span></span>

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

### <span data-ttu-id="80fd6-127">-역할</span><span class="sxs-lookup"><span data-stu-id="80fd6-127">-Role</span></span>
<span data-ttu-id="80fd6-128">업데이트할 역할 정의 개체</span><span class="sxs-lookup"><span data-stu-id="80fd6-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="80fd6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80fd6-129">CommonParameters</span></span>
<span data-ttu-id="80fd6-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80fd6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80fd6-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80fd6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80fd6-132">입력</span><span class="sxs-lookup"><span data-stu-id="80fd6-132">INPUTS</span></span>

### <span data-ttu-id="80fd6-133">Microsoft. a. PSRoleDefinition (.Resources.</span><span class="sxs-lookup"><span data-stu-id="80fd6-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="80fd6-134">매개 변수: Role (ByValue)</span><span class="sxs-lookup"><span data-stu-id="80fd6-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="80fd6-135">출력</span><span class="sxs-lookup"><span data-stu-id="80fd6-135">OUTPUTS</span></span>

### <span data-ttu-id="80fd6-136">Microsoft. a. PSRoleDefinition (.Resources.</span><span class="sxs-lookup"><span data-stu-id="80fd6-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="80fd6-137">상속자</span><span class="sxs-lookup"><span data-stu-id="80fd6-137">NOTES</span></span>
<span data-ttu-id="80fd6-138">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="80fd6-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="80fd6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80fd6-139">RELATED LINKS</span></span>

[<span data-ttu-id="80fd6-140">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="80fd6-140">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="80fd6-141">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="80fd6-141">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="80fd6-142">새로운 AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="80fd6-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="80fd6-143">제거-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="80fd6-143">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

