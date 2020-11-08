---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 947D1C09-7CFA-4E97-A6B3-2DA9D7507F0C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0260b452c96b5f6dd60599b5da15cc323b5423d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046263"
---
# <span data-ttu-id="a547e-101">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="a547e-101">Get-WAPackVNet</span></span>

## <span data-ttu-id="a547e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a547e-102">SYNOPSIS</span></span>
<span data-ttu-id="a547e-103">가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a547e-103">Gets virtual networks.</span></span>

## <span data-ttu-id="a547e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a547e-104">SYNTAX</span></span>

### <span data-ttu-id="a547e-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a547e-105">Empty (Default)</span></span>
```
Get-WAPackVNet [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a547e-106">찡그린 Mid</span><span class="sxs-lookup"><span data-stu-id="a547e-106">FromId</span></span>
```
Get-WAPackVNet -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a547e-107">FromName</span><span class="sxs-lookup"><span data-stu-id="a547e-107">FromName</span></span>
```
Get-WAPackVNet -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a547e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a547e-108">DESCRIPTION</span></span>
<span data-ttu-id="a547e-109">**Get-WAPackVNet** cmdlet은 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a547e-109">The **Get-WAPackVNet** cmdlet gets virtual networks.</span></span>

## <span data-ttu-id="a547e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a547e-110">EXAMPLES</span></span>

### <span data-ttu-id="a547e-111">예제 1: 모든 가상 네트워크 가져오기</span><span class="sxs-lookup"><span data-stu-id="a547e-111">Example 1: Get all virtual networks</span></span>
```
PS C:\> Get-WAPackVNet
```

<span data-ttu-id="a547e-112">이 명령은 모든 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a547e-112">This command gets all virtual networks.</span></span>

### <span data-ttu-id="a547e-113">예제 2: ID를 사용 하 여 가상 네트워크 가져오기</span><span class="sxs-lookup"><span data-stu-id="a547e-113">Example 2: Get a virtual network by using an ID</span></span>
```
PS C:\> Get-WAPackVNet -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="a547e-114">이 명령은 지정 된 ID를 가진 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a547e-114">This command gets the virtual network that has the specified ID.</span></span>

### <span data-ttu-id="a547e-115">예제 3: 이름을 사용 하 여 가상 네트워크 가져오기</span><span class="sxs-lookup"><span data-stu-id="a547e-115">Example 3: Get a virtual network by using a name</span></span>
```
PS C:\> Get-WAPackVNet -Name "ContosoVNet08"
```

<span data-ttu-id="a547e-116">이 명령은 ContosoVNet08 이라는 가상 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a547e-116">This command gets the virtual network named ContosoVNet08.</span></span>

## <span data-ttu-id="a547e-117">변수</span><span class="sxs-lookup"><span data-stu-id="a547e-117">PARAMETERS</span></span>

### <span data-ttu-id="a547e-118">-ID</span><span class="sxs-lookup"><span data-stu-id="a547e-118">-ID</span></span>
<span data-ttu-id="a547e-119">가상 네트워크의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a547e-119">Specifies the unique ID of a virtual network.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="a547e-120">-Name</span></span>
<span data-ttu-id="a547e-121">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a547e-121">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a547e-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="a547e-122">-Profile</span></span>
<span data-ttu-id="a547e-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a547e-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a547e-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a547e-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a547e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a547e-125">CommonParameters</span></span>
<span data-ttu-id="a547e-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a547e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a547e-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a547e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a547e-128">입력</span><span class="sxs-lookup"><span data-stu-id="a547e-128">INPUTS</span></span>

## <span data-ttu-id="a547e-129">출력</span><span class="sxs-lookup"><span data-stu-id="a547e-129">OUTPUTS</span></span>

## <span data-ttu-id="a547e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a547e-130">NOTES</span></span>

## <span data-ttu-id="a547e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a547e-131">RELATED LINKS</span></span>

