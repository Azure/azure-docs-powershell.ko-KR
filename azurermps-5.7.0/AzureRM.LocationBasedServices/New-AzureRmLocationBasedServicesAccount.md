---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 739ce121e26f1010c5c13ff3330dadffa02053af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528127"
---
# <span data-ttu-id="36246-101">New-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="36246-101">New-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="36246-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36246-102">SYNOPSIS</span></span>
<span data-ttu-id="36246-103">위치 기반 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="36246-103">Creates a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36246-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36246-104">SYNTAX</span></span>

```
New-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36246-105">설명은</span><span class="sxs-lookup"><span data-stu-id="36246-105">DESCRIPTION</span></span>
<span data-ttu-id="36246-106">**AzureRmLocationBasedServicesAccount** cmdlet은 지정 된 SKU를 사용 하 여 Location 기반 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="36246-106">The **New-AzureRmLocationBasedServicesAccount** cmdlet creates a Location Based Services account with the specified SKU.</span></span>

## <span data-ttu-id="36246-107">예제의</span><span class="sxs-lookup"><span data-stu-id="36246-107">EXAMPLES</span></span>

### <span data-ttu-id="36246-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="36246-108">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

Notice
By creating a Location Based Account, you are consenting to the terms of use (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="36246-109">SKU S0 및 tag를 사용 하 여 리소스 그룹 MyResourceGroup에 내 계정 이라는 새 위치 기반 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="36246-109">Creates a new Location Based Services account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="36246-110">변수</span><span class="sxs-lookup"><span data-stu-id="36246-110">PARAMETERS</span></span>

### <span data-ttu-id="36246-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36246-111">-DefaultProfile</span></span>
<span data-ttu-id="36246-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36246-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36246-113">-Force</span><span class="sxs-lookup"><span data-stu-id="36246-113">-Force</span></span>
<span data-ttu-id="36246-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36246-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="36246-115">-이름</span><span class="sxs-lookup"><span data-stu-id="36246-115">-Name</span></span>
<span data-ttu-id="36246-116">위치 기반 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36246-116">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36246-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36246-117">-ResourceGroupName</span></span>
<span data-ttu-id="36246-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36246-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36246-119">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="36246-119">-SkuName</span></span>
<span data-ttu-id="36246-120">위치 기반 서비스 계정 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36246-120">Location Based Services Account Sku Name.</span></span>

<span data-ttu-id="36246-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="36246-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36246-122">S0</span><span class="sxs-lookup"><span data-stu-id="36246-122">S0</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36246-123">태그</span><span class="sxs-lookup"><span data-stu-id="36246-123">-Tag</span></span>
<span data-ttu-id="36246-124">위치 기반 서비스 계정 태그</span><span class="sxs-lookup"><span data-stu-id="36246-124">Location Based Services Account Tags.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36246-125">-확인</span><span class="sxs-lookup"><span data-stu-id="36246-125">-Confirm</span></span>
<span data-ttu-id="36246-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="36246-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36246-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36246-127">-WhatIf</span></span>
<span data-ttu-id="36246-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="36246-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36246-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="36246-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36246-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36246-130">CommonParameters</span></span>
<span data-ttu-id="36246-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36246-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36246-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36246-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36246-133">입력</span><span class="sxs-lookup"><span data-stu-id="36246-133">INPUTS</span></span>

### <span data-ttu-id="36246-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="36246-134">System.String</span></span>

## <span data-ttu-id="36246-135">출력</span><span class="sxs-lookup"><span data-stu-id="36246-135">OUTPUTS</span></span>

### <span data-ttu-id="36246-136">LocationBasedServices. PSLocationBasedServicesAccount/.</span><span class="sxs-lookup"><span data-stu-id="36246-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>

## <span data-ttu-id="36246-137">상속자</span><span class="sxs-lookup"><span data-stu-id="36246-137">NOTES</span></span>

<span data-ttu-id="36246-138">위치 기반 서비스 계정을 만들려면 약관을 수락 하 라는 메시지에 응답 해야 합니다 (참조) https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/) .</span><span class="sxs-lookup"><span data-stu-id="36246-138">Creating a Location Based Services account requires answering a prompt to accept terms (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).</span></span>  <span data-ttu-id="36246-139">-Force 매개 변수를 사용 하 여 조건의 수락을 나타낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36246-139">The -Force parameter can be used to indicate acceptance of the terms.</span></span>

## <span data-ttu-id="36246-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36246-140">RELATED LINKS</span></span>
