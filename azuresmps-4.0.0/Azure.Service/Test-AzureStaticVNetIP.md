---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E059EF1-740C-4AEB-AF41-BF6003BE15F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: a52f2585771ec10d6acf52b14c88bd1ed0af0427
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045936"
---
# <span data-ttu-id="c8d3c-101">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="c8d3c-101">Test-AzureStaticVNetIP</span></span>

## <span data-ttu-id="c8d3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d3c-103">정적 가상 네트워크 IP 주소의 가용성을 테스트 하 고, 쿼리 된 주소를 사용할 수 없는 경우 추천 단어 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c8d3c-103">Tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="c8d3c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c8d3c-104">SYNTAX</span></span>

```
Test-AzureStaticVNetIP [-VNetName] <String> [-IPAddress] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8d3c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c8d3c-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d3c-106">**테스트-AzureStaticVNetIP** cmdlet은 정적 가상 네트워크 IP 주소의 가용성을 테스트 하 고 쿼리 된 주소를 사용할 수 없는 경우 제안 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c8d3c-106">The **Test-AzureStaticVNetIP** cmdlet tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="c8d3c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c8d3c-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d3c-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="c8d3c-108">1:</span></span>
```

```

## <span data-ttu-id="c8d3c-109">변수</span><span class="sxs-lookup"><span data-stu-id="c8d3c-109">PARAMETERS</span></span>

### <span data-ttu-id="c8d3c-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c8d3c-110">-InformationAction</span></span>
<span data-ttu-id="c8d3c-111">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d3c-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c8d3c-112">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c8d3c-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8d3c-113">하기로</span><span class="sxs-lookup"><span data-stu-id="c8d3c-113">Continue</span></span>
- <span data-ttu-id="c8d3c-114">숨기기</span><span class="sxs-lookup"><span data-stu-id="c8d3c-114">Ignore</span></span>
- <span data-ttu-id="c8d3c-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="c8d3c-115">Inquire</span></span>
- <span data-ttu-id="c8d3c-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8d3c-116">SilentlyContinue</span></span>
- <span data-ttu-id="c8d3c-117">중지가</span><span class="sxs-lookup"><span data-stu-id="c8d3c-117">Stop</span></span>
- <span data-ttu-id="c8d3c-118">대기</span><span class="sxs-lookup"><span data-stu-id="c8d3c-118">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d3c-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8d3c-119">-InformationVariable</span></span>
<span data-ttu-id="c8d3c-120">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d3c-120">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d3c-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="c8d3c-121">-IPAddress</span></span>
<span data-ttu-id="c8d3c-122">쿼리할 정적 가상 네트워크 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d3c-122">Specifies the static virtual network IP address to query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d3c-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="c8d3c-123">-Profile</span></span>
<span data-ttu-id="c8d3c-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d3c-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c8d3c-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c8d3c-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c8d3c-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c8d3c-126">-VNetName</span></span>
<span data-ttu-id="c8d3c-127">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d3c-127">Specifies the Name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8d3c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d3c-128">CommonParameters</span></span>
<span data-ttu-id="c8d3c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d3c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d3c-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d3c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d3c-131">입력</span><span class="sxs-lookup"><span data-stu-id="c8d3c-131">INPUTS</span></span>

## <span data-ttu-id="c8d3c-132">출력</span><span class="sxs-lookup"><span data-stu-id="c8d3c-132">OUTPUTS</span></span>

## <span data-ttu-id="c8d3c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c8d3c-133">NOTES</span></span>

## <span data-ttu-id="c8d3c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8d3c-134">RELATED LINKS</span></span>

[<span data-ttu-id="c8d3c-135">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="c8d3c-135">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="c8d3c-136">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="c8d3c-136">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


