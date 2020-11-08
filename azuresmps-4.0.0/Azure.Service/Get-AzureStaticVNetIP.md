---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 12BF47AA-9E82-425E-A1EB-BAD64D800943
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3be6496993ed6de248103b9a222df4cbe15ed2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046557"
---
# <span data-ttu-id="5dd26-101">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="5dd26-101">Get-AzureStaticVNetIP</span></span>

## <span data-ttu-id="5dd26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dd26-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd26-103">가상 머신 개체 (있는 경우)에서 정적 VNet IP 주소 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd26-103">Gets the static VNet IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="5dd26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5dd26-104">SYNTAX</span></span>

```
Get-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5dd26-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5dd26-105">DESCRIPTION</span></span>
<span data-ttu-id="5dd26-106">**Get-AzureStaticVNetIP** cmdlet은 가상 머신 개체 (있는 경우)의 VNet (정적 가상 네트워크) IP 주소 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd26-106">The **Get-AzureStaticVNetIP** cmdlet gets the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="5dd26-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5dd26-107">EXAMPLES</span></span>

### <span data-ttu-id="5dd26-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="5dd26-108">1:</span></span>
```

```

## <span data-ttu-id="5dd26-109">변수</span><span class="sxs-lookup"><span data-stu-id="5dd26-109">PARAMETERS</span></span>

### <span data-ttu-id="5dd26-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5dd26-110">-InformationAction</span></span>
<span data-ttu-id="5dd26-111">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd26-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5dd26-112">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5dd26-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5dd26-113">하기로</span><span class="sxs-lookup"><span data-stu-id="5dd26-113">Continue</span></span>
- <span data-ttu-id="5dd26-114">숨기기</span><span class="sxs-lookup"><span data-stu-id="5dd26-114">Ignore</span></span>
- <span data-ttu-id="5dd26-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="5dd26-115">Inquire</span></span>
- <span data-ttu-id="5dd26-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5dd26-116">SilentlyContinue</span></span>
- <span data-ttu-id="5dd26-117">중지가</span><span class="sxs-lookup"><span data-stu-id="5dd26-117">Stop</span></span>
- <span data-ttu-id="5dd26-118">대기</span><span class="sxs-lookup"><span data-stu-id="5dd26-118">Suspend</span></span>

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

### <span data-ttu-id="5dd26-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5dd26-119">-InformationVariable</span></span>
<span data-ttu-id="5dd26-120">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd26-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5dd26-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="5dd26-121">-Profile</span></span>
<span data-ttu-id="5dd26-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd26-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5dd26-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5dd26-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5dd26-124">-VM</span><span class="sxs-lookup"><span data-stu-id="5dd26-124">-VM</span></span>
<span data-ttu-id="5dd26-125">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd26-125">Specifies a persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dd26-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd26-126">CommonParameters</span></span>
<span data-ttu-id="5dd26-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd26-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd26-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dd26-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd26-129">입력</span><span class="sxs-lookup"><span data-stu-id="5dd26-129">INPUTS</span></span>

## <span data-ttu-id="5dd26-130">출력</span><span class="sxs-lookup"><span data-stu-id="5dd26-130">OUTPUTS</span></span>

## <span data-ttu-id="5dd26-131">상속자</span><span class="sxs-lookup"><span data-stu-id="5dd26-131">NOTES</span></span>

## <span data-ttu-id="5dd26-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dd26-132">RELATED LINKS</span></span>

[<span data-ttu-id="5dd26-133">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="5dd26-133">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


