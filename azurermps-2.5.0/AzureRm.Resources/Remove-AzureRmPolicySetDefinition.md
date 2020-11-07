---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
ms.openlocfilehash: 1096dc42ce02f3255c3c144852fc13029aebd113
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882773"
---
# <span data-ttu-id="459fd-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="459fd-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="459fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="459fd-102">SYNOPSIS</span></span>
<span data-ttu-id="459fd-103">정책 집합 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="459fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="459fd-104">SYNTAX</span></span>

### <span data-ttu-id="459fd-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="459fd-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="459fd-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="459fd-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="459fd-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="459fd-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="459fd-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="459fd-108">IdParameterSet</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="459fd-109">설명은</span><span class="sxs-lookup"><span data-stu-id="459fd-109">DESCRIPTION</span></span>
<span data-ttu-id="459fd-110">**제거-AzureRmPolicySetDefinition** cmdlet은 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-110">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="459fd-111">예제의</span><span class="sxs-lookup"><span data-stu-id="459fd-111">EXAMPLES</span></span>

### <span data-ttu-id="459fd-112">예제 1: 리소스 ID 별 정책 집합 정의 제거</span><span class="sxs-lookup"><span data-stu-id="459fd-112">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="459fd-113">첫 번째 명령은 Get-AzureRmPolicySetDefinition cmdlet을 사용 하 여 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="459fd-114">명령이 $PolicySetDefinition 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-114">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="459fd-115">두 번째 명령은 $PolicySetDefinition의 **ResourceId** 속성으로 식별 되는 정책 집합 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-115">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="459fd-116">변수</span><span class="sxs-lookup"><span data-stu-id="459fd-116">PARAMETERS</span></span>

### <span data-ttu-id="459fd-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="459fd-117">-ApiVersion</span></span>
<span data-ttu-id="459fd-118">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="459fd-119">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-119">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="459fd-120">-DefaultProfile</span></span>
<span data-ttu-id="459fd-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="459fd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="459fd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="459fd-122">-Force</span></span>
<span data-ttu-id="459fd-123">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-123">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-124">-Id</span><span class="sxs-lookup"><span data-stu-id="459fd-124">-Id</span></span>
<span data-ttu-id="459fd-125">구독을 포함 하는 정규화 된 정책 집합 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-125">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="459fd-126">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="459fd-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="459fd-127">-ManagementGroupName</span></span>
<span data-ttu-id="459fd-128">삭제할 정책 집합 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-128">The name of the management group of the policy set definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-129">-이름</span><span class="sxs-lookup"><span data-stu-id="459fd-129">-Name</span></span>
<span data-ttu-id="459fd-130">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-130">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="459fd-131">-Pre</span></span>
<span data-ttu-id="459fd-132">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="459fd-133">-SubscriptionId</span></span>
<span data-ttu-id="459fd-134">삭제할 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-134">The subscription ID of the policy set definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-135">-확인</span><span class="sxs-lookup"><span data-stu-id="459fd-135">-Confirm</span></span>
<span data-ttu-id="459fd-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="459fd-137">-WhatIf</span></span>
<span data-ttu-id="459fd-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="459fd-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="459fd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="459fd-140">CommonParameters</span></span>
<span data-ttu-id="459fd-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="459fd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="459fd-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="459fd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="459fd-143">입력</span><span class="sxs-lookup"><span data-stu-id="459fd-143">INPUTS</span></span>

### <span data-ttu-id="459fd-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="459fd-144">System.String</span></span>

### <span data-ttu-id="459fd-145">시스템 Null 허용 ' 1 [[b77a5c561934e089], mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="459fd-145">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="459fd-146">출력</span><span class="sxs-lookup"><span data-stu-id="459fd-146">OUTPUTS</span></span>

### <span data-ttu-id="459fd-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="459fd-147">System.Boolean</span></span>

## <span data-ttu-id="459fd-148">상속자</span><span class="sxs-lookup"><span data-stu-id="459fd-148">NOTES</span></span>

## <span data-ttu-id="459fd-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="459fd-149">RELATED LINKS</span></span>
