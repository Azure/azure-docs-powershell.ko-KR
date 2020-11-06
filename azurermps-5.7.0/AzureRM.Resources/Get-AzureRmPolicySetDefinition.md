---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533644"
---
# <span data-ttu-id="1836f-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1836f-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="1836f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1836f-102">SYNOPSIS</span></span>
<span data-ttu-id="1836f-103">정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1836f-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1836f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1836f-104">SYNTAX</span></span>

### <span data-ttu-id="1836f-105">GetBySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="1836f-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1836f-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1836f-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1836f-107">GetById</span><span class="sxs-lookup"><span data-stu-id="1836f-107">GetById</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1836f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1836f-108">DESCRIPTION</span></span>
<span data-ttu-id="1836f-109">**AzureRmPolicySetDefinition** cmdlet은 모든 정책 집합 정의 또는 이름 또는 ID로 식별 되는 특정 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1836f-109">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="1836f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1836f-110">EXAMPLES</span></span>

### <span data-ttu-id="1836f-111">예제 1: 모든 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="1836f-111">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="1836f-112">이 명령은 모든 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1836f-112">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="1836f-113">예제 2: 이름별로 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="1836f-113">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="1836f-114">이 명령은 VMPolicyDefinition 이라는 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1836f-114">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="1836f-115">변수</span><span class="sxs-lookup"><span data-stu-id="1836f-115">PARAMETERS</span></span>

### <span data-ttu-id="1836f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1836f-116">-ApiVersion</span></span>
<span data-ttu-id="1836f-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1836f-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1836f-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1836f-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1836f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1836f-119">-DefaultProfile</span></span>
<span data-ttu-id="1836f-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1836f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1836f-121">-Id</span><span class="sxs-lookup"><span data-stu-id="1836f-121">-Id</span></span>
<span data-ttu-id="1836f-122">구독을 포함 하는 정규화 된 정책 집합 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1836f-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="1836f-123">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1836f-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1836f-124">-이름</span><span class="sxs-lookup"><span data-stu-id="1836f-124">-Name</span></span>
<span data-ttu-id="1836f-125">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1836f-125">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1836f-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="1836f-126">-Pre</span></span>
<span data-ttu-id="1836f-127">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1836f-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1836f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1836f-128">CommonParameters</span></span>
<span data-ttu-id="1836f-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1836f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1836f-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1836f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1836f-131">입력</span><span class="sxs-lookup"><span data-stu-id="1836f-131">INPUTS</span></span>

### <span data-ttu-id="1836f-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1836f-132">System.String</span></span>

## <span data-ttu-id="1836f-133">출력</span><span class="sxs-lookup"><span data-stu-id="1836f-133">OUTPUTS</span></span>

### <span data-ttu-id="1836f-134">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="1836f-134">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1836f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="1836f-135">NOTES</span></span>

## <span data-ttu-id="1836f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1836f-136">RELATED LINKS</span></span>
