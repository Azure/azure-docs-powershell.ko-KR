---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: fa96d686d66f9ef94322896974dc4dd3b81ad154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531664"
---
# <span data-ttu-id="b0a80-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b0a80-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="b0a80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a80-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a80-103">정책 집합 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0a80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0a80-104">SYNTAX</span></span>

### <span data-ttu-id="b0a80-105">RemoveByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="b0a80-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a80-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="b0a80-106">RemoveById</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0a80-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b0a80-107">DESCRIPTION</span></span>
<span data-ttu-id="b0a80-108">**제거-AzureRmPolicySetDefinition** cmdlet은 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-108">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="b0a80-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b0a80-109">EXAMPLES</span></span>

### <span data-ttu-id="b0a80-110">예제 1: 리소스 ID 별 정책 집합 정의 제거</span><span class="sxs-lookup"><span data-stu-id="b0a80-110">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="b0a80-111">첫 번째 명령은 Get-AzureRmPolicySetDefinition cmdlet을 사용 하 여 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="b0a80-112">명령이 $PolicySetDefinition 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-112">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="b0a80-113">두 번째 명령은 $PolicySetDefinition의 **ResourceId** 속성으로 식별 되는 정책 집합 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-113">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="b0a80-114">변수</span><span class="sxs-lookup"><span data-stu-id="b0a80-114">PARAMETERS</span></span>

### <span data-ttu-id="b0a80-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b0a80-115">-ApiVersion</span></span>
<span data-ttu-id="b0a80-116">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b0a80-117">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a80-118">-DefaultProfile</span></span>
<span data-ttu-id="b0a80-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b0a80-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a80-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b0a80-120">-Force</span></span>
<span data-ttu-id="b0a80-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a80-122">-Id</span><span class="sxs-lookup"><span data-stu-id="b0a80-122">-Id</span></span>
<span data-ttu-id="b0a80-123">구독을 포함 하는 정규화 된 정책 집합 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-123">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="b0a80-124">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b0a80-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a80-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b0a80-125">-Name</span></span>
<span data-ttu-id="b0a80-126">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-126">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0a80-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="b0a80-127">-Pre</span></span>
<span data-ttu-id="b0a80-128">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a80-129">-확인</span><span class="sxs-lookup"><span data-stu-id="b0a80-129">-Confirm</span></span>
<span data-ttu-id="b0a80-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a80-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0a80-131">-WhatIf</span></span>
<span data-ttu-id="b0a80-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0a80-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a80-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a80-134">CommonParameters</span></span>
<span data-ttu-id="b0a80-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a80-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a80-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0a80-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a80-137">입력</span><span class="sxs-lookup"><span data-stu-id="b0a80-137">INPUTS</span></span>

### <span data-ttu-id="b0a80-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b0a80-138">System.String</span></span>

## <span data-ttu-id="b0a80-139">출력</span><span class="sxs-lookup"><span data-stu-id="b0a80-139">OUTPUTS</span></span>

### <span data-ttu-id="b0a80-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b0a80-140">System.Boolean</span></span>

## <span data-ttu-id="b0a80-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b0a80-141">NOTES</span></span>

## <span data-ttu-id="b0a80-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0a80-142">RELATED LINKS</span></span>
