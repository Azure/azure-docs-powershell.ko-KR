---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046375"
---
# <span data-ttu-id="2448c-101">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2448c-101">Enable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="2448c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2448c-102">SYNOPSIS</span></span>
<span data-ttu-id="2448c-103">Traffic Manager 프로필을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="2448c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2448c-104">SYNTAX</span></span>

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2448c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2448c-105">DESCRIPTION</span></span>
<span data-ttu-id="2448c-106">AzureTrafficManagerProfile cmdlet을 **사용** 하면 Microsoft Azure Traffic Manager 프로필을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-106">The **Enable-AzureTrafficManagerProfile** cmdlet enables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="2448c-107">작업의 성공 여부를 표시 하는 *PassThru* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-107">Specify the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="2448c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2448c-108">EXAMPLES</span></span>

### <span data-ttu-id="2448c-109">예제 1: Traffic Manager 프로필 사용</span><span class="sxs-lookup"><span data-stu-id="2448c-109">Example 1: Enable a Traffic Manager profile</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="2448c-110">이 명령은 MyProfile 이라는 Traffic Manager 프로필을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-110">This command enables the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="2448c-111">예제 2: Traffic Manager 프로필을 사용 하도록 설정 하 고 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2448c-111">Example 2: Enable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="2448c-112">이 명령은 MyProfile 이라는 Traffic Manager 프로필을 사용 하도록 설정 하 고 명령이 성공적으로 수행 되었는지 여부를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-112">This command enables the Traffic Manager profile named MyProfile and displays whether the command succeeded.</span></span>

## <span data-ttu-id="2448c-113">변수</span><span class="sxs-lookup"><span data-stu-id="2448c-113">PARAMETERS</span></span>

### <span data-ttu-id="2448c-114">-이름</span><span class="sxs-lookup"><span data-stu-id="2448c-114">-Name</span></span>
<span data-ttu-id="2448c-115">사용할 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-115">Specifies the name of the Traffic Manager profile to enable.</span></span>

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

### <span data-ttu-id="2448c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2448c-116">-PassThru</span></span>
<span data-ttu-id="2448c-117">작업이 성공한 경우 $True를 반환 하 고, 그렇지 않으면 그렇지 않으면 $False 합니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-117">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="2448c-118">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2448c-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="2448c-119">-Profile</span></span>
<span data-ttu-id="2448c-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-120">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2448c-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2448c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2448c-122">CommonParameters</span></span>
<span data-ttu-id="2448c-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2448c-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2448c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2448c-125">입력</span><span class="sxs-lookup"><span data-stu-id="2448c-125">INPUTS</span></span>

## <span data-ttu-id="2448c-126">출력</span><span class="sxs-lookup"><span data-stu-id="2448c-126">OUTPUTS</span></span>

### <span data-ttu-id="2448c-127">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2448c-127">System.Boolean</span></span>
<span data-ttu-id="2448c-128">이 cmdlet은 $True 또는 $False를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-128">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="2448c-129">작업이 성공 하 고 *PassThru* 매개 변수를 지정 하면이 cmdlet은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2448c-129">If the operation succeeds and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="2448c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="2448c-130">NOTES</span></span>

## <span data-ttu-id="2448c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2448c-131">RELATED LINKS</span></span>

[<span data-ttu-id="2448c-132">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2448c-132">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2448c-133">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2448c-133">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2448c-134">새로운 AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2448c-134">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2448c-135">제거-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2448c-135">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2448c-136">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2448c-136">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


