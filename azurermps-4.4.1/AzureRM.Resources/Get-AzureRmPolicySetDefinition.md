---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 5fba45e50076952a0a2e11e2e5541ab9546d3bc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533004"
---
# <span data-ttu-id="fef32-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="fef32-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="fef32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fef32-102">SYNOPSIS</span></span>
<span data-ttu-id="fef32-103">정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fef32-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fef32-104">SYNTAX</span></span>

### <span data-ttu-id="fef32-105">모든 정책 집합 정의 매개 변수 집합 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-105">The list all policy set definitions parameter set.</span></span> <span data-ttu-id="fef32-106">기본값</span><span class="sxs-lookup"><span data-stu-id="fef32-106">(Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fef32-107">정책 집합 정의 이름 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="fef32-107">The policy set definition name parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fef32-108">정책 집합 정의 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="fef32-108">The policy set definition Id parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fef32-109">설명은</span><span class="sxs-lookup"><span data-stu-id="fef32-109">DESCRIPTION</span></span>
<span data-ttu-id="fef32-110">**AzureRmPolicySetDefinition** cmdlet은 모든 정책 집합 정의 또는 이름 또는 ID로 식별 되는 특정 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-110">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="fef32-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fef32-111">EXAMPLES</span></span>

### <span data-ttu-id="fef32-112">예제 1: 모든 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="fef32-112">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="fef32-113">이 명령은 모든 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-113">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="fef32-114">예제 2: 이름별로 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="fef32-114">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="fef32-115">이 명령은 VMPolicyDefinition 이라는 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-115">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="fef32-116">변수</span><span class="sxs-lookup"><span data-stu-id="fef32-116">PARAMETERS</span></span>

### <span data-ttu-id="fef32-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fef32-117">-ApiVersion</span></span>
<span data-ttu-id="fef32-118">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fef32-119">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fef32-120">-Id</span><span class="sxs-lookup"><span data-stu-id="fef32-120">-Id</span></span>
<span data-ttu-id="fef32-121">구독을 포함 하는 정규화 된 정책 집합 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-121">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="fef32-122">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="fef32-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef32-123">-이름</span><span class="sxs-lookup"><span data-stu-id="fef32-123">-Name</span></span>
<span data-ttu-id="fef32-124">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-124">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef32-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="fef32-125">-Pre</span></span>
<span data-ttu-id="fef32-126">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fef32-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef32-127">-DefaultProfile</span></span>
<span data-ttu-id="fef32-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fef32-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef32-129">CommonParameters</span></span>
<span data-ttu-id="fef32-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fef32-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef32-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef32-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef32-132">입력</span><span class="sxs-lookup"><span data-stu-id="fef32-132">INPUTS</span></span>

### <span data-ttu-id="fef32-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fef32-133">System.String</span></span>

## <span data-ttu-id="fef32-134">출력</span><span class="sxs-lookup"><span data-stu-id="fef32-134">OUTPUTS</span></span>

### <span data-ttu-id="fef32-135">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="fef32-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fef32-136">상속자</span><span class="sxs-lookup"><span data-stu-id="fef32-136">NOTES</span></span>

## <span data-ttu-id="fef32-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fef32-137">RELATED LINKS</span></span>

