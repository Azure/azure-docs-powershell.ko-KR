---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 16a27c7756a25c4b8e4270a0c363f8a04528d12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524940"
---
# <span data-ttu-id="385c9-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="385c9-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="385c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="385c9-102">SYNOPSIS</span></span>
<span data-ttu-id="385c9-103">정책 집합 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="385c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="385c9-104">SYNTAX</span></span>

### <span data-ttu-id="385c9-105">SetByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="385c9-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="385c9-106">SetById</span><span class="sxs-lookup"><span data-stu-id="385c9-106">SetById</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="385c9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="385c9-107">DESCRIPTION</span></span>
<span data-ttu-id="385c9-108">**Set-AzureRmPolicySetDefinition** cmdlet은 정책 정의를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-108">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="385c9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="385c9-109">EXAMPLES</span></span>

### <span data-ttu-id="385c9-110">예제 1: 정책 집합 정의에 대 한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="385c9-110">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="385c9-111">첫 번째 명령은 Get-AzureRmPolicySetDefinition cmdlet을 사용 하 여 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="385c9-112">명령이 $PolicySetDefinition 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-112">The command stores that object in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="385c9-113">두 번째 명령은 $PolicySetDefinition의 **ResourceId** 속성으로 식별 되는 정책 집합 정의에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-113">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="385c9-114">변수</span><span class="sxs-lookup"><span data-stu-id="385c9-114">PARAMETERS</span></span>

### <span data-ttu-id="385c9-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="385c9-115">-ApiVersion</span></span>
<span data-ttu-id="385c9-116">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="385c9-117">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="385c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385c9-118">-DefaultProfile</span></span>
<span data-ttu-id="385c9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="385c9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="385c9-120">-설명</span><span class="sxs-lookup"><span data-stu-id="385c9-120">-Description</span></span>
<span data-ttu-id="385c9-121">정책 집합 정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-121">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385c9-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="385c9-122">-DisplayName</span></span>
<span data-ttu-id="385c9-123">정책 집합 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-123">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385c9-124">-Id</span><span class="sxs-lookup"><span data-stu-id="385c9-124">-Id</span></span>
<span data-ttu-id="385c9-125">구독을 포함 하는 정규화 된 정책 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-125">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="385c9-126">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="385c9-126">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385c9-127">-이름</span><span class="sxs-lookup"><span data-stu-id="385c9-127">-Name</span></span>
<span data-ttu-id="385c9-128">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-128">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385c9-129">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="385c9-129">-PolicyDefinition</span></span>
<span data-ttu-id="385c9-130">정책 집합 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-130">The policy set definition.</span></span> <span data-ttu-id="385c9-131">이는 정책 정의를 포함 하는 파일 이름에 대 한 경로 이거나 정책 집합 정의를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-131">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="385c9-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="385c9-132">-Pre</span></span>
<span data-ttu-id="385c9-133">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="385c9-134">-확인</span><span class="sxs-lookup"><span data-stu-id="385c9-134">-Confirm</span></span>
<span data-ttu-id="385c9-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="385c9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="385c9-136">-WhatIf</span></span>
<span data-ttu-id="385c9-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="385c9-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="385c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385c9-139">CommonParameters</span></span>
<span data-ttu-id="385c9-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="385c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385c9-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385c9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385c9-142">입력</span><span class="sxs-lookup"><span data-stu-id="385c9-142">INPUTS</span></span>

### <span data-ttu-id="385c9-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="385c9-143">System.String</span></span>

## <span data-ttu-id="385c9-144">출력</span><span class="sxs-lookup"><span data-stu-id="385c9-144">OUTPUTS</span></span>

### <span data-ttu-id="385c9-145">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="385c9-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="385c9-146">상속자</span><span class="sxs-lookup"><span data-stu-id="385c9-146">NOTES</span></span>

## <span data-ttu-id="385c9-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="385c9-147">RELATED LINKS</span></span>
