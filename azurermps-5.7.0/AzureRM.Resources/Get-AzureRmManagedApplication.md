---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 3dd86c186d05ce59f237be51b8e059e800c47a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703234"
---
# <span data-ttu-id="40845-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="40845-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="40845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40845-102">SYNOPSIS</span></span>
<span data-ttu-id="40845-103">관리 되는 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40845-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40845-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40845-104">SYNTAX</span></span>

### <span data-ttu-id="40845-105">GetBySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="40845-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40845-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40845-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40845-107">GetById</span><span class="sxs-lookup"><span data-stu-id="40845-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40845-108">설명은</span><span class="sxs-lookup"><span data-stu-id="40845-108">DESCRIPTION</span></span>
<span data-ttu-id="40845-109">**Get-AzureRmManagedApplication** cmdlet은 관리 되는 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40845-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="40845-110">예제의</span><span class="sxs-lookup"><span data-stu-id="40845-110">EXAMPLES</span></span>

### <span data-ttu-id="40845-111">예제 1: 리소스 그룹 아래에 모든 관리 되는 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="40845-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="40845-112">이 명령은 리소스 그룹 "MyRG"에서 관리 되는 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40845-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="40845-113">예제 2: 관리 되는 모든 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="40845-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="40845-114">이 명령은 현재 구독에서 관리 되는 모든 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="40845-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="40845-115">변수</span><span class="sxs-lookup"><span data-stu-id="40845-115">PARAMETERS</span></span>

### <span data-ttu-id="40845-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="40845-116">-ApiVersion</span></span>
<span data-ttu-id="40845-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="40845-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="40845-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40845-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="40845-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40845-119">-DefaultProfile</span></span>
<span data-ttu-id="40845-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40845-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40845-121">-Id</span><span class="sxs-lookup"><span data-stu-id="40845-121">-Id</span></span>
<span data-ttu-id="40845-122">구독을 포함 하는 정규화 된 관리 되는 응용 프로그램 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="40845-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="40845-123">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="40845-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40845-124">-이름</span><span class="sxs-lookup"><span data-stu-id="40845-124">-Name</span></span>
<span data-ttu-id="40845-125">관리 되는 응용 프로그램 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40845-125">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40845-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="40845-126">-Pre</span></span>
<span data-ttu-id="40845-127">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="40845-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="40845-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40845-128">-ResourceGroupName</span></span>
<span data-ttu-id="40845-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40845-129">The resource group name.</span></span>

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

### <span data-ttu-id="40845-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40845-130">CommonParameters</span></span>
<span data-ttu-id="40845-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40845-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40845-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40845-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40845-133">입력</span><span class="sxs-lookup"><span data-stu-id="40845-133">INPUTS</span></span>

### <span data-ttu-id="40845-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40845-134">System.String</span></span>

## <span data-ttu-id="40845-135">출력</span><span class="sxs-lookup"><span data-stu-id="40845-135">OUTPUTS</span></span>

### <span data-ttu-id="40845-136">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="40845-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="40845-137">상속자</span><span class="sxs-lookup"><span data-stu-id="40845-137">NOTES</span></span>

## <span data-ttu-id="40845-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40845-138">RELATED LINKS</span></span>
