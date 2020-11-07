---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: 4c4bbd9dd845caa263f5dd333228d71e3f2e65b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703330"
---
# <span data-ttu-id="11884-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="11884-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="11884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11884-102">SYNOPSIS</span></span>
<span data-ttu-id="11884-103">할당에 사용할 수 있는 모든 Azure RBAC 역할을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="11884-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11884-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11884-104">SYNTAX</span></span>

### <span data-ttu-id="11884-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11884-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11884-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11884-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11884-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="11884-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11884-108">설명은</span><span class="sxs-lookup"><span data-stu-id="11884-108">DESCRIPTION</span></span>
<span data-ttu-id="11884-109">특정 역할 이름과 함께 Get-AzureRmRoleDefinition 명령을 사용 하 여 세부 정보를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="11884-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="11884-110">역할이 액세스를 허용 하는 개별 작업을 검사 하려면 해당 역할의 작업 및 NotActions 속성을 검토 합니다.</span><span class="sxs-lookup"><span data-stu-id="11884-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="11884-111">예제의</span><span class="sxs-lookup"><span data-stu-id="11884-111">EXAMPLES</span></span>

### <span data-ttu-id="11884-112">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="11884-112">--------------------------  Example 1  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="11884-113">읽기 프로그램 역할 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="11884-113">Get the Reader role definition</span></span>

### <span data-ttu-id="11884-114">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="11884-114">--------------------------  Example 2  --------------------------</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="11884-115">모든 RBAC 역할 정의를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="11884-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="11884-116">변수</span><span class="sxs-lookup"><span data-stu-id="11884-116">PARAMETERS</span></span>

### <span data-ttu-id="11884-117">-AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="11884-117">-AtScopeAndBelow</span></span>
<span data-ttu-id="11884-118">지정 된 경우 모든 역할 정의를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11884-118">If specified, displays all role definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11884-119">-사용자 지정</span><span class="sxs-lookup"><span data-stu-id="11884-119">-Custom</span></span>
<span data-ttu-id="11884-120">지정 된 경우 디렉터리에 사용자 지정 만들기 역할만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11884-120">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="11884-121">-Id</span><span class="sxs-lookup"><span data-stu-id="11884-121">-Id</span></span>
<span data-ttu-id="11884-122">역할 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="11884-122">Role definition Id.</span></span>

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

### <span data-ttu-id="11884-123">-이름</span><span class="sxs-lookup"><span data-stu-id="11884-123">-Name</span></span>
<span data-ttu-id="11884-124">역할 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11884-124">Role definition name.</span></span>
<span data-ttu-id="11884-125">예를 들어 독자, 참가자, 가상 컴퓨터 참가자.</span><span class="sxs-lookup"><span data-stu-id="11884-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="11884-126">-범위</span><span class="sxs-lookup"><span data-stu-id="11884-126">-Scope</span></span>
<span data-ttu-id="11884-127">역할 정의 범위</span><span class="sxs-lookup"><span data-stu-id="11884-127">Role definition scope.</span></span>

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

### <span data-ttu-id="11884-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11884-128">-DefaultProfile</span></span>
<span data-ttu-id="11884-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11884-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11884-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11884-130">CommonParameters</span></span>
<span data-ttu-id="11884-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11884-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11884-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11884-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11884-133">입력</span><span class="sxs-lookup"><span data-stu-id="11884-133">INPUTS</span></span>

### <span data-ttu-id="11884-134">이름</span><span class="sxs-lookup"><span data-stu-id="11884-134">String</span></span>
<span data-ttu-id="11884-135">' Scope ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="11884-135">Parameter 'Scope' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="11884-136">출력</span><span class="sxs-lookup"><span data-stu-id="11884-136">OUTPUTS</span></span>

### <span data-ttu-id="11884-137">System.webserver. List ' 1 [Microsoft. t e m. a n a] ... PSRoleDefinition (권한 집합)</span><span class="sxs-lookup"><span data-stu-id="11884-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition]</span></span>

## <span data-ttu-id="11884-138">상속자</span><span class="sxs-lookup"><span data-stu-id="11884-138">NOTES</span></span>
<span data-ttu-id="11884-139">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="11884-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="11884-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11884-140">RELATED LINKS</span></span>

[<span data-ttu-id="11884-141">새로운 AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="11884-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="11884-142">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="11884-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="11884-143">새로운 AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="11884-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="11884-144">제거-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="11884-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

