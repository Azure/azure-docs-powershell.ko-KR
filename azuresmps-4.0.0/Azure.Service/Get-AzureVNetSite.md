---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046527"
---
# <span data-ttu-id="50ab2-101">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="50ab2-101">Get-AzureVNetSite</span></span>

## <span data-ttu-id="50ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="50ab2-103">Azure 가상 네트워크에 대 한 정보가 포함 된 목록 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-103">Gets a list object with information about Azure virtual networks.</span></span>

## <span data-ttu-id="50ab2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50ab2-104">SYNTAX</span></span>

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="50ab2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="50ab2-105">DESCRIPTION</span></span>
<span data-ttu-id="50ab2-106">**Get-AzureVNetSite** cmdlet은 현재 구독의 Azure 가상 네트워크에 대 한 정보가 포함 된 목록 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-106">The **Get-AzureVNetSite** cmdlet gets a list object with information about Azure virtual networks for the current subscription.</span></span>
<span data-ttu-id="50ab2-107">가상 네트워크 이름을 지정 하면 해당 가상 네트워크에 대 한 정보만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-107">If you specify a virtual network name, only information for that virtual network is returned.</span></span>

## <span data-ttu-id="50ab2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="50ab2-108">EXAMPLES</span></span>

### <span data-ttu-id="50ab2-109">예제 1: 현재 구독의 모든 가상 네트워크에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="50ab2-109">Example 1: Get information about all virtual networks in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite
```

<span data-ttu-id="50ab2-110">이 명령은 현재 구독의 모든 가상 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-110">This command gets information about all the virtual networks in the current subscription.</span></span>

### <span data-ttu-id="50ab2-111">예제 2: 현재 구독의 특정 가상 네트워크에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="50ab2-111">Example 2: Get information about a specific virtual network in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

<span data-ttu-id="50ab2-112">이 명령은 MyProductionNetwork 가상 네트워크에 대 한 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-112">This command retrieves information on the MyProductionNetwork virtual network only.</span></span>

## <span data-ttu-id="50ab2-113">변수</span><span class="sxs-lookup"><span data-stu-id="50ab2-113">PARAMETERS</span></span>

### <span data-ttu-id="50ab2-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="50ab2-114">-InformationAction</span></span>
<span data-ttu-id="50ab2-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="50ab2-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="50ab2-117">하기로</span><span class="sxs-lookup"><span data-stu-id="50ab2-117">Continue</span></span>
- <span data-ttu-id="50ab2-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="50ab2-118">Ignore</span></span>
- <span data-ttu-id="50ab2-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="50ab2-119">Inquire</span></span>
- <span data-ttu-id="50ab2-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="50ab2-120">SilentlyContinue</span></span>
- <span data-ttu-id="50ab2-121">중지가</span><span class="sxs-lookup"><span data-stu-id="50ab2-121">Stop</span></span>
- <span data-ttu-id="50ab2-122">대기</span><span class="sxs-lookup"><span data-stu-id="50ab2-122">Suspend</span></span>

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

### <span data-ttu-id="50ab2-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="50ab2-123">-InformationVariable</span></span>
<span data-ttu-id="50ab2-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="50ab2-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="50ab2-125">-Profile</span></span>
<span data-ttu-id="50ab2-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50ab2-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50ab2-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="50ab2-128">-VNetName</span></span>
<span data-ttu-id="50ab2-129">정보를 반환할 가상 네트워크 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-129">Specifies a virtual network name to return information about.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50ab2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ab2-130">CommonParameters</span></span>
<span data-ttu-id="50ab2-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50ab2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ab2-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50ab2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ab2-133">입력</span><span class="sxs-lookup"><span data-stu-id="50ab2-133">INPUTS</span></span>

## <span data-ttu-id="50ab2-134">출력</span><span class="sxs-lookup"><span data-stu-id="50ab2-134">OUTPUTS</span></span>

## <span data-ttu-id="50ab2-135">상속자</span><span class="sxs-lookup"><span data-stu-id="50ab2-135">NOTES</span></span>

## <span data-ttu-id="50ab2-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50ab2-136">RELATED LINKS</span></span>

[<span data-ttu-id="50ab2-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="50ab2-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="50ab2-138">-AzureVNetConfig 제거</span><span class="sxs-lookup"><span data-stu-id="50ab2-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="50ab2-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="50ab2-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


