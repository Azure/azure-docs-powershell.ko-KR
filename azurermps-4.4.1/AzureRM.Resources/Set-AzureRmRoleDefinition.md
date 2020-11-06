---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 9f5927905e492fd93998e12f97a97a0380755905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530703"
---
# <span data-ttu-id="97fd3-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="97fd3-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="97fd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="97fd3-103">Azure RBAC의 사용자 지정 역할을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="97fd3-104">수정 된 역할 정의를 JSON 파일 또는 PSRoleDefinition으로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="97fd3-105">먼저 Get-AzureRmRoleDefinition 명령을 사용 하 여 수정할 사용자 지정 역할을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="97fd3-106">그런 다음 변경할 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="97fd3-107">마지막으로,이 명령을 사용 하 여 역할 정의를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97fd3-108">구문과</span><span class="sxs-lookup"><span data-stu-id="97fd3-108">SYNTAX</span></span>

### <span data-ttu-id="97fd3-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="97fd3-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97fd3-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="97fd3-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97fd3-111">설명은</span><span class="sxs-lookup"><span data-stu-id="97fd3-111">DESCRIPTION</span></span>
<span data-ttu-id="97fd3-112">Set-AzureRmRoleDefinition cmdlet은 Azure Role-Based Access Control의 기존 사용자 지정 역할을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="97fd3-113">업데이트 된 역할 정의를 JSON 파일 또는 PSRoleDefinition 개체로 명령에 대 한 입력으로 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="97fd3-114">업데이트 된 사용자 지정 역할에 대 한 역할 정의에는 이름, 설명, 동작, AssignableScopes 업데이트 되지 않은 경우에도 해당 역할의 Id 및 기타 모든 필수 속성이 포함 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="97fd3-115">NotActions는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-115">NotActions is optional.</span></span>

<span data-ttu-id="97fd3-116">다음은 Set-AzureRmRoleDefinition에 대 한 업데이트 된 역할 정의 json 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition</span></span>

<span data-ttu-id="97fd3-117">{"Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "이름": "업데이트 된 역할", "설명": "모든 리소스를 모니터링 하 고 가상 컴퓨터를 시작 하 고 다시 시작할 수 있습니다.", "작업": \[ "\*/read", "ClassicCompute/virtualmachines/restart/action", "Microsoft. ClassicCompute/virtualmachines/start/action" \] "AssignableScopes": \[ "/subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f" \] }</span><span class="sxs-lookup"><span data-stu-id="97fd3-117">{ "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "\*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] "AssignableScopes": \["/subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f"\] }</span></span>

## <span data-ttu-id="97fd3-118">예제의</span><span class="sxs-lookup"><span data-stu-id="97fd3-118">EXAMPLES</span></span>

### <span data-ttu-id="97fd3-119">PSRoleDefinitionObject를 사용 하 여--------------------------업데이트--------------------------</span><span class="sxs-lookup"><span data-stu-id="97fd3-119">--------------------------  Update using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/eb910d4f-edbf-429b-94F6-d76bae7ff401", "/subscriptions/a846d197-5eac-45c7-b885-a6227fe6d388")

          PS C:\> New-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="97fd3-120">JSON 파일을 사용 하 여 만들기----------------------------------------------------</span><span class="sxs-lookup"><span data-stu-id="97fd3-120">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="97fd3-121">변수</span><span class="sxs-lookup"><span data-stu-id="97fd3-121">PARAMETERS</span></span>

### <span data-ttu-id="97fd3-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="97fd3-122">-InputFile</span></span>
<span data-ttu-id="97fd3-123">업데이트 될 단일 json 역할 정의가 포함 된 파일 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-123">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="97fd3-124">JSON에서 업데이트 되는 속성만 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-124">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="97fd3-125">Id 속성이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-125">Id property is Required.</span></span>

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

### <span data-ttu-id="97fd3-126">-역할</span><span class="sxs-lookup"><span data-stu-id="97fd3-126">-Role</span></span>
<span data-ttu-id="97fd3-127">업데이트할 역할 정의 개체</span><span class="sxs-lookup"><span data-stu-id="97fd3-127">Role definition object to be updated</span></span>

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

### <span data-ttu-id="97fd3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97fd3-128">-DefaultProfile</span></span>
<span data-ttu-id="97fd3-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97fd3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97fd3-130">CommonParameters</span></span>
<span data-ttu-id="97fd3-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97fd3-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97fd3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97fd3-133">입력</span><span class="sxs-lookup"><span data-stu-id="97fd3-133">INPUTS</span></span>

### <span data-ttu-id="97fd3-134">PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="97fd3-134">PSRoleDefinition</span></span>
<span data-ttu-id="97fd3-135">' Role ' 매개 변수는 파이프라인에서 ' PSRoleDefinition ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd3-135">Parameter 'Role' accepts value of type 'PSRoleDefinition' from the pipeline</span></span>

## <span data-ttu-id="97fd3-136">출력</span><span class="sxs-lookup"><span data-stu-id="97fd3-136">OUTPUTS</span></span>

### <span data-ttu-id="97fd3-137">Microsoft. a. PSRoleDefinition (.Resources.</span><span class="sxs-lookup"><span data-stu-id="97fd3-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="97fd3-138">상속자</span><span class="sxs-lookup"><span data-stu-id="97fd3-138">NOTES</span></span>
<span data-ttu-id="97fd3-139">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="97fd3-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="97fd3-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97fd3-140">RELATED LINKS</span></span>

[<span data-ttu-id="97fd3-141">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="97fd3-141">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="97fd3-142">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="97fd3-142">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="97fd3-143">새로운 AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="97fd3-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="97fd3-144">제거-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="97fd3-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

