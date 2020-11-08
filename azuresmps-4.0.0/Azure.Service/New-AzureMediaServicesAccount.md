---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045911"
---
# <span data-ttu-id="b86a6-101">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b86a6-101">New-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="b86a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b86a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b86a6-103">Azure 미디어 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-103">Creates an Azure Media Services account.</span></span>

<span data-ttu-id="b86a6-104">**참고:** 이 버전은 더 이상 사용 되지 않습니다. [최신 버전](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="b86a6-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="b86a6-105">구문과</span><span class="sxs-lookup"><span data-stu-id="b86a6-105">SYNTAX</span></span>

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b86a6-106">설명은</span><span class="sxs-lookup"><span data-stu-id="b86a6-106">DESCRIPTION</span></span>
<span data-ttu-id="b86a6-107">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b86a6-108">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b86a6-109">**AzureMediaServicesAccount** cmdlet은 지정 된 미디어 서비스 계정 이름, 계정을 만들려는 데이터 센터 위치, 기존 저장소 계정 이름을 사용 하 여 새 미디어 서비스 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-109">The **New-AzureMediaServicesAccount** cmdlet creates a new Media Services account with the specified Media Services account name, datacenter location where you want to create the account, and an existing storage account name.</span></span>
<span data-ttu-id="b86a6-110">저장소 계정은 새 미디어 서비스 계정과 동일한 데이터 센터에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-110">The storage account has to be located in the same data center as the new Media Services account.</span></span>

## <span data-ttu-id="b86a6-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b86a6-111">EXAMPLES</span></span>

### <span data-ttu-id="b86a6-112">예제 1: 새 미디어 서비스 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="b86a6-112">Example 1: Create a new Media Services account</span></span>
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## <span data-ttu-id="b86a6-113">변수</span><span class="sxs-lookup"><span data-stu-id="b86a6-113">PARAMETERS</span></span>

### <span data-ttu-id="b86a6-114">-위치</span><span class="sxs-lookup"><span data-stu-id="b86a6-114">-Location</span></span>
<span data-ttu-id="b86a6-115">미디어 서비스 데이터 센터 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-115">Specifies the Media Services datacenter location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86a6-116">-이름</span><span class="sxs-lookup"><span data-stu-id="b86a6-116">-Name</span></span>
<span data-ttu-id="b86a6-117">미디어 서비스 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-117">Specifies the Media Services account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86a6-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="b86a6-118">-Profile</span></span>
<span data-ttu-id="b86a6-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b86a6-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b86a6-121">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b86a6-121">-StorageAccountName</span></span>
<span data-ttu-id="b86a6-122">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-122">Specifies the storage account name.</span></span>
<span data-ttu-id="b86a6-123">저장소 계정이 새 미디어 서비스 계정과 같은 데이터 센터에 이미 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-123">The storage account must already exist in the same datacenter as the new Media Services account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b86a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b86a6-124">CommonParameters</span></span>
<span data-ttu-id="b86a6-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b86a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b86a6-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b86a6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b86a6-127">입력</span><span class="sxs-lookup"><span data-stu-id="b86a6-127">INPUTS</span></span>

## <span data-ttu-id="b86a6-128">출력</span><span class="sxs-lookup"><span data-stu-id="b86a6-128">OUTPUTS</span></span>

## <span data-ttu-id="b86a6-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b86a6-129">NOTES</span></span>

## <span data-ttu-id="b86a6-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b86a6-130">RELATED LINKS</span></span>

[<span data-ttu-id="b86a6-131">미디어 서비스에 Azure PowerShell을 사용 하는 방법</span><span class="sxs-lookup"><span data-stu-id="b86a6-131">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="b86a6-132">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b86a6-132">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="b86a6-133">제거-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="b86a6-133">Remove-AzureMediaServicesAccount</span></span>](./Remove-AzureMediaServicesAccount.md)


