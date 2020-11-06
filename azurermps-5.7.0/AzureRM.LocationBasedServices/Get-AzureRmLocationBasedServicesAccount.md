---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528934"
---
# <span data-ttu-id="257f9-101">Get-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="257f9-101">Get-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="257f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="257f9-102">SYNOPSIS</span></span>
<span data-ttu-id="257f9-103">계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="257f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="257f9-104">SYNTAX</span></span>

### <span data-ttu-id="257f9-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="257f9-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="257f9-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="257f9-106">AccountNameParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="257f9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="257f9-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="257f9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="257f9-108">DESCRIPTION</span></span>
<span data-ttu-id="257f9-109">**AzureRmLocationBasedServicesAccount** cmdlet은 리소스 그룹과 이름 또는 리소스 id를 기준으로 프로 비전 된 위치 기반 서비스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-109">The **Get-AzureRmLocationBasedServicesAccount** cmdlet gets a provisioned Location Based Services account, either by resource group and name, or by resource id.</span></span>

<span data-ttu-id="257f9-110">또한이는 ResourceGroup의 모든 계정 목록 또는 현재 구독에 대 한 모든 위치 기반 서비스 계정을 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-110">Additionally, it can return a list of all accounts in the ResourceGroup, or all Location Based Services accounts for the current subscription.</span></span>

## <span data-ttu-id="257f9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="257f9-111">EXAMPLES</span></span>

### <span data-ttu-id="257f9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="257f9-112">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="257f9-113">리소스 그룹 MyResourceGroup에 내 계정 이라는 계정이 있는 경우 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-113">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="257f9-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="257f9-114">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="257f9-115">리소스 그룹 MyResourceGroup의 모든 위치 기반 서비스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-115">Gets all Location Based Services accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="257f9-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="257f9-116">Example 3</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="257f9-117">현재 구독에서 모든 Location 기반 서비스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-117">Gets all Location Based Services accounts in the current subscription.</span></span>

### <span data-ttu-id="257f9-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="257f9-118">Example 4</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="257f9-119">리소스 Id로 지정 된 위치 기반 서비스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-119">Gets the Location Based Services account specified by the Resource Id.</span></span>

## <span data-ttu-id="257f9-120">변수</span><span class="sxs-lookup"><span data-stu-id="257f9-120">PARAMETERS</span></span>

### <span data-ttu-id="257f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257f9-121">-DefaultProfile</span></span>
<span data-ttu-id="257f9-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="257f9-123">-이름</span><span class="sxs-lookup"><span data-stu-id="257f9-123">-Name</span></span>
<span data-ttu-id="257f9-124">위치 기반 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-124">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="257f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="257f9-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257f9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="257f9-127">-ResourceId</span></span>
<span data-ttu-id="257f9-128">위치 기반 서비스 계정 ResourceId.</span><span class="sxs-lookup"><span data-stu-id="257f9-128">Location Based Services Account ResourceId.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="257f9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257f9-129">CommonParameters</span></span>
<span data-ttu-id="257f9-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257f9-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="257f9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257f9-132">입력</span><span class="sxs-lookup"><span data-stu-id="257f9-132">INPUTS</span></span>

### <span data-ttu-id="257f9-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="257f9-133">System.String</span></span>

## <span data-ttu-id="257f9-134">출력</span><span class="sxs-lookup"><span data-stu-id="257f9-134">OUTPUTS</span></span>

### <span data-ttu-id="257f9-135">LocationBasedServices. PSLocationBasedServicesAccount/.</span><span class="sxs-lookup"><span data-stu-id="257f9-135">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>
<span data-ttu-id="257f9-136">이 cmdlet은 **PSLocationBasedServicesAccount** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-136">This cmdlet returns a **PSLocationBasedServicesAccount** object.</span></span>
<span data-ttu-id="257f9-137">이 개체를 수정한 다음 **Set-AzureRmLocationBasedServices** 를 사용 하 여 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="257f9-137">You can modify this object, and then apply changes by using **Set-AzureRmLocationBasedServices**.</span></span>

## <span data-ttu-id="257f9-138">상속자</span><span class="sxs-lookup"><span data-stu-id="257f9-138">NOTES</span></span>

## <span data-ttu-id="257f9-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="257f9-139">RELATED LINKS</span></span>
