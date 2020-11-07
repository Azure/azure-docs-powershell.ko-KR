---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: d43ec874af02d57abedddb1b49b3cc8723af5c2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876461"
---
# <span data-ttu-id="830d9-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="830d9-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="830d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="830d9-102">SYNOPSIS</span></span>
<span data-ttu-id="830d9-103">할당에 사용할 수 있는 모든 Azure RBAC 역할을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="830d9-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="830d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="830d9-104">SYNTAX</span></span>

### <span data-ttu-id="830d9-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="830d9-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="830d9-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="830d9-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="830d9-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="830d9-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="830d9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="830d9-108">DESCRIPTION</span></span>
<span data-ttu-id="830d9-109">특정 역할 이름과 함께 Get-AzRoleDefinition 명령을 사용 하 여 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="830d9-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="830d9-110">역할이 액세스를 허용 하는 개별 작업을 검사 하려면 해당 역할의 작업 및 NotActions 속성을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="830d9-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="830d9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="830d9-111">EXAMPLES</span></span>

### <span data-ttu-id="830d9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="830d9-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="830d9-113">읽기 프로그램 역할 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="830d9-113">Get the Reader role definition</span></span>

### <span data-ttu-id="830d9-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="830d9-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="830d9-115">모든 RBAC 역할 정의를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="830d9-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="830d9-116">변수</span><span class="sxs-lookup"><span data-stu-id="830d9-116">PARAMETERS</span></span>

### <span data-ttu-id="830d9-117">-사용자 지정</span><span class="sxs-lookup"><span data-stu-id="830d9-117">-Custom</span></span>
<span data-ttu-id="830d9-118">지정 된 경우 디렉터리에 사용자 지정 만들기 역할만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="830d9-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830d9-119">-DefaultProfile</span></span>
<span data-ttu-id="830d9-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="830d9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830d9-121">-Id</span><span class="sxs-lookup"><span data-stu-id="830d9-121">-Id</span></span>
<span data-ttu-id="830d9-122">역할 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="830d9-122">Role definition Id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830d9-123">-이름</span><span class="sxs-lookup"><span data-stu-id="830d9-123">-Name</span></span>
<span data-ttu-id="830d9-124">역할 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="830d9-124">Role definition name.</span></span>
<span data-ttu-id="830d9-125">예를 들어 독자, 참가자, 가상 컴퓨터 참가자.</span><span class="sxs-lookup"><span data-stu-id="830d9-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830d9-126">-범위</span><span class="sxs-lookup"><span data-stu-id="830d9-126">-Scope</span></span>
<span data-ttu-id="830d9-127">역할 정의 범위</span><span class="sxs-lookup"><span data-stu-id="830d9-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="830d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830d9-128">CommonParameters</span></span>
<span data-ttu-id="830d9-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="830d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830d9-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="830d9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830d9-131">입력</span><span class="sxs-lookup"><span data-stu-id="830d9-131">INPUTS</span></span>

### <span data-ttu-id="830d9-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="830d9-132">System.String</span></span>
<span data-ttu-id="830d9-133">매개 변수: Scope (ByValue)</span><span class="sxs-lookup"><span data-stu-id="830d9-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="830d9-134">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="830d9-134">System.Guid</span></span>

### <span data-ttu-id="830d9-135">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="830d9-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="830d9-136">출력</span><span class="sxs-lookup"><span data-stu-id="830d9-136">OUTPUTS</span></span>

### <span data-ttu-id="830d9-137">Microsoft. a. PSRoleDefinition (.Resources.</span><span class="sxs-lookup"><span data-stu-id="830d9-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="830d9-138">상속자</span><span class="sxs-lookup"><span data-stu-id="830d9-138">NOTES</span></span>
<span data-ttu-id="830d9-139">키워드: azure, Az, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="830d9-139">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="830d9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="830d9-140">RELATED LINKS</span></span>

[<span data-ttu-id="830d9-141">새로운 AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="830d9-141">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="830d9-142">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="830d9-142">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="830d9-143">새로운 AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="830d9-143">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="830d9-144">제거-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="830d9-144">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

