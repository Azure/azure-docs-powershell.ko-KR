---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046330"
---
# <span data-ttu-id="99d98-101">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="99d98-101">Get-AzureRemoteAppCollectionUsageSummary</span></span>

## <span data-ttu-id="99d98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d98-102">SYNOPSIS</span></span>
<span data-ttu-id="99d98-103">Azure RemoteApp 컬렉션에 대 한 사용 요약을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-103">Retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="99d98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99d98-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99d98-105">설명은</span><span class="sxs-lookup"><span data-stu-id="99d98-105">DESCRIPTION</span></span>
<span data-ttu-id="99d98-106">**AzureRemoteAppCollectionUsageSummary** Cmdlet은 Azure RemoteApp 컬렉션에 대 한 사용 요약을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-106">The **Get-AzureRemoteAppCollectionUsageSummary** cmdlet retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="99d98-107">예제의</span><span class="sxs-lookup"><span data-stu-id="99d98-107">EXAMPLES</span></span>

### <span data-ttu-id="99d98-108">예제 1: 사용 현황 요약 가져오기</span><span class="sxs-lookup"><span data-stu-id="99d98-108">Example 1: Get a usage summary</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="99d98-109">이 명령은 Contoso 라는 컬렉션에 대해 2014 년 12 월에 대 한 사용 요약 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-109">This command gets a usage summary for the month of December in the year 2014, for a collection named Contoso.</span></span>

## <span data-ttu-id="99d98-110">변수</span><span class="sxs-lookup"><span data-stu-id="99d98-110">PARAMETERS</span></span>

### <span data-ttu-id="99d98-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="99d98-111">-CollectionName</span></span>
<span data-ttu-id="99d98-112">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="99d98-113">-프로필</span><span class="sxs-lookup"><span data-stu-id="99d98-113">-Profile</span></span>
<span data-ttu-id="99d98-114">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="99d98-115">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99d98-116">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="99d98-116">-UsageMonth</span></span>
<span data-ttu-id="99d98-117">사용 현황 요약을 가져올 월의 두 자리 숫자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-117">Specifies a two digit number for the month for which to get a usage summary.</span></span>
<span data-ttu-id="99d98-118">이 매개 변수를 지정 하지 않으면이 cmdlet은 현재 달에 대 한 사용을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-118">If this parameter is not specified, this cmdlet provides usage for the current month.</span></span>

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

### <span data-ttu-id="99d98-119">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="99d98-119">-UsageYear</span></span>
<span data-ttu-id="99d98-120">사용 현황 요약을 가져올 네 자리 연도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-120">Specifies the four-digit year for which to get a usage summary.</span></span>
<span data-ttu-id="99d98-121">이 매개 변수를 지정 하지 않으면이 cmdlet은 현재 연도에 대 한 사용 요약을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-121">If this parameter is not specified, this cmdlet provides a usage summary for the current year will be used.</span></span>

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

### <span data-ttu-id="99d98-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d98-122">CommonParameters</span></span>
<span data-ttu-id="99d98-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99d98-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d98-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d98-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d98-125">입력</span><span class="sxs-lookup"><span data-stu-id="99d98-125">INPUTS</span></span>

## <span data-ttu-id="99d98-126">출력</span><span class="sxs-lookup"><span data-stu-id="99d98-126">OUTPUTS</span></span>

## <span data-ttu-id="99d98-127">상속자</span><span class="sxs-lookup"><span data-stu-id="99d98-127">NOTES</span></span>

## <span data-ttu-id="99d98-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99d98-128">RELATED LINKS</span></span>

[<span data-ttu-id="99d98-129">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="99d98-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="99d98-130">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="99d98-130">Get-AzureRemoteAppCollectionUsageDetails</span></span>](./Get-AzureRemoteAppCollectionUsageDetails.md)


