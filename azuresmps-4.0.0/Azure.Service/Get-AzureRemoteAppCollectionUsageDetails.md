---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 0E5F05B3-F2B0-479C-8222-927C34140416
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74892352afe02ae5eb2f19e05704c23c489d2d75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045632"
---
# <span data-ttu-id="65e51-101">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="65e51-101">Get-AzureRemoteAppCollectionUsageDetails</span></span>

## <span data-ttu-id="65e51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65e51-102">SYNOPSIS</span></span>
<span data-ttu-id="65e51-103">Azure RemoteApp 컬렉션에 대 한 사용 세부 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e51-103">Retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="65e51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65e51-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageDetails [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-AsJob] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65e51-105">설명은</span><span class="sxs-lookup"><span data-stu-id="65e51-105">DESCRIPTION</span></span>
<span data-ttu-id="65e51-106">**AzureRemoteAppCollectionUsageDetails** Cmdlet은 Azure RemoteApp 컬렉션에 대 한 사용 세부 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e51-106">The **Get-AzureRemoteAppCollectionUsageDetails** cmdlet retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="65e51-107">예제의</span><span class="sxs-lookup"><span data-stu-id="65e51-107">EXAMPLES</span></span>

### <span data-ttu-id="65e51-108">예제 1: 컬렉션에 대 한 사용 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="65e51-108">Example 1: Get usage details for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageDetails -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="65e51-109">이 명령은 2014 년의 12 월에 대 한 사용 세부 정보를 가져오며,이는 Contoso 라는 Azure RemoteApp 컬렉션에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e51-109">This command gets usage details for the month of December in the year 2014, for an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="65e51-110">변수</span><span class="sxs-lookup"><span data-stu-id="65e51-110">PARAMETERS</span></span>

### <span data-ttu-id="65e51-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65e51-111">-AsJob</span></span>
<span data-ttu-id="65e51-112">Cmdlet이 Windows PowerShell 작업으로 백그라운드에서 실행 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="65e51-112">Indicates that the cmdlet runs in the background as a Windows PowerShell job.</span></span>

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

### <span data-ttu-id="65e51-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="65e51-113">-CollectionName</span></span>
<span data-ttu-id="65e51-114">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e51-114">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65e51-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="65e51-115">-Profile</span></span>
<span data-ttu-id="65e51-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e51-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65e51-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="65e51-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65e51-118">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="65e51-118">-UsageMonth</span></span>
<span data-ttu-id="65e51-119">사용 세부 정보를 가져올 월의 두 자리 숫자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e51-119">Specifies a two-digit number for the month for which to get usage details.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e51-120">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="65e51-120">-UsageYear</span></span>
<span data-ttu-id="65e51-121">사용 세부 정보를 가져올 네 자리 연도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e51-121">Specifies the four-digit year for which to get usage details.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e51-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e51-122">CommonParameters</span></span>
<span data-ttu-id="65e51-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e51-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e51-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e51-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e51-125">입력</span><span class="sxs-lookup"><span data-stu-id="65e51-125">INPUTS</span></span>

## <span data-ttu-id="65e51-126">출력</span><span class="sxs-lookup"><span data-stu-id="65e51-126">OUTPUTS</span></span>

## <span data-ttu-id="65e51-127">상속자</span><span class="sxs-lookup"><span data-stu-id="65e51-127">NOTES</span></span>

## <span data-ttu-id="65e51-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65e51-128">RELATED LINKS</span></span>

[<span data-ttu-id="65e51-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="65e51-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="65e51-130">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="65e51-130">Get-AzureRemoteAppCollectionUsageSummary</span></span>](./Get-AzureRemoteAppCollectionUsageSummary.md)


