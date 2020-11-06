---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536772"
---
# <span data-ttu-id="13a1b-101">Get-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="13a1b-101">Get-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="13a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="13a1b-103">계정에 대 한 API 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-103">Gets the API keys for an account.</span></span> <span data-ttu-id="13a1b-104">이러한 키는 Azure 위치 기반 서비스에 대 한 후속 호출에 사용 되는 인증 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-104">These keys are the authentication mechanism used in subsequent calls to Azure Location Based Services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13a1b-105">구문과</span><span class="sxs-lookup"><span data-stu-id="13a1b-105">SYNTAX</span></span>

### <span data-ttu-id="13a1b-106">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="13a1b-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13a1b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13a1b-107">InputObjectParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13a1b-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="13a1b-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13a1b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="13a1b-109">DESCRIPTION</span></span>
<span data-ttu-id="13a1b-110">**AzureRmLocationBasedServicesAccountKey** cmdlet은 프로 비전 된 위치 기반 서비스 계정에 대 한 API 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-110">The **Get-AzureRmLocationBasedServicesAccountKey** cmdlet gets the API keys for a provisioned Location Based Services account.</span></span>

<span data-ttu-id="13a1b-111">위치 기반 서비스 계정에는 기본 및 보조의 두 가지 API 키가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-111">A Location Based Services account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="13a1b-112">키를 사용 하 여 위치 기반 서비스 계정 끝점과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-112">The keys enable interaction with the Location Based Services account endpoint.</span></span>

<span data-ttu-id="13a1b-113">[New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) 를 사용 하 여 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) to regenerate a key.</span></span>

## <span data-ttu-id="13a1b-114">예제의</span><span class="sxs-lookup"><span data-stu-id="13a1b-114">EXAMPLES</span></span>

### <span data-ttu-id="13a1b-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="13a1b-115">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="13a1b-116">리소스 그룹 MyResourceGroup의 내 계정 이라는 계정에 대 한 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="13a1b-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="13a1b-117">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="13a1b-118">지정 된 위치 기반 서비스 계정에 대 한 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-118">Returns the keys for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="13a1b-119">변수</span><span class="sxs-lookup"><span data-stu-id="13a1b-119">PARAMETERS</span></span>

### <span data-ttu-id="13a1b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a1b-120">-DefaultProfile</span></span>
<span data-ttu-id="13a1b-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13a1b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13a1b-122">-InputObject</span></span>
<span data-ttu-id="13a1b-123">Location 기반 서비스 계정이 [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md)에서 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-123">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13a1b-124">-이름</span><span class="sxs-lookup"><span data-stu-id="13a1b-124">-Name</span></span>
<span data-ttu-id="13a1b-125">위치 기반 서비스 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-125">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a1b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a1b-126">-ResourceGroupName</span></span>
<span data-ttu-id="13a1b-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13a1b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13a1b-128">-ResourceId</span></span>
<span data-ttu-id="13a1b-129">위치 기반 서비스 계정 ResourceId.</span><span class="sxs-lookup"><span data-stu-id="13a1b-129">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="13a1b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a1b-130">CommonParameters</span></span>
<span data-ttu-id="13a1b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a1b-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a1b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a1b-133">입력</span><span class="sxs-lookup"><span data-stu-id="13a1b-133">INPUTS</span></span>

### <span data-ttu-id="13a1b-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13a1b-134">System.String</span></span>

## <span data-ttu-id="13a1b-135">출력</span><span class="sxs-lookup"><span data-stu-id="13a1b-135">OUTPUTS</span></span>

### <span data-ttu-id="13a1b-136">LocationBasedServices. PSLocationBasedServicesAccountKeys/.</span><span class="sxs-lookup"><span data-stu-id="13a1b-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccountKeys</span></span>

### <span data-ttu-id="13a1b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a1b-137">CommonParameters</span></span>
<span data-ttu-id="13a1b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13a1b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a1b-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a1b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a1b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="13a1b-140">NOTES</span></span>

## <span data-ttu-id="13a1b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13a1b-141">RELATED LINKS</span></span>
