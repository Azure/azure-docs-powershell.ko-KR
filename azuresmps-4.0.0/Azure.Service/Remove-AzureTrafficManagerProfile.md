---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046091"
---
# <span data-ttu-id="c672e-101">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c672e-101">Remove-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="c672e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c672e-102">SYNOPSIS</span></span>
<span data-ttu-id="c672e-103">Traffic Manager 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-103">Removes a Traffic Manager profile.</span></span>

## <span data-ttu-id="c672e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c672e-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c672e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c672e-105">DESCRIPTION</span></span>
<span data-ttu-id="c672e-106">**AzureTrafficManagerProfile** cmdlet은 현재 구독에서 Microsoft Azure Traffic Manager 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-106">The **Remove-AzureTrafficManagerProfile** cmdlet removes a Microsoft Azure Traffic Manager profile from the current subscription.</span></span>

## <span data-ttu-id="c672e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c672e-107">EXAMPLES</span></span>

### <span data-ttu-id="c672e-108">예제 1: Traffic Manager 프로필 제거</span><span class="sxs-lookup"><span data-stu-id="c672e-108">Example 1: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="c672e-109">이 명령은 MyProfile 이라는 Traffic Manager 프로필을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-109">This command removes the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="c672e-110">예제 2: Traffic Manager 프로필 제거</span><span class="sxs-lookup"><span data-stu-id="c672e-110">Example 2: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

<span data-ttu-id="c672e-111">이 명령은 사용자에 게 확인 메시지를 표시 하지 않고 MyProfile 이라는 Traffic Manager 프로필을 제거 하 고 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-111">This command removes the Traffic Manager profile named MyProfile without prompting you for confirmation, and returns the results.</span></span>

## <span data-ttu-id="c672e-112">변수</span><span class="sxs-lookup"><span data-stu-id="c672e-112">PARAMETERS</span></span>

### <span data-ttu-id="c672e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c672e-113">-Force</span></span>
<span data-ttu-id="c672e-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c672e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c672e-115">-Name</span></span>
<span data-ttu-id="c672e-116">삭제할 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-116">Specifies the name of the Traffic Manager profile to delete.</span></span>

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

### <span data-ttu-id="c672e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c672e-117">-PassThru</span></span>
<span data-ttu-id="c672e-118">작업이 성공한 경우 $True를 반환 하 고, 그렇지 않으면 그렇지 않으면 $False 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="c672e-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c672e-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="c672e-120">-Profile</span></span>
<span data-ttu-id="c672e-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c672e-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c672e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c672e-123">CommonParameters</span></span>
<span data-ttu-id="c672e-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c672e-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c672e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c672e-126">입력</span><span class="sxs-lookup"><span data-stu-id="c672e-126">INPUTS</span></span>

## <span data-ttu-id="c672e-127">출력</span><span class="sxs-lookup"><span data-stu-id="c672e-127">OUTPUTS</span></span>

### <span data-ttu-id="c672e-128">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c672e-128">System.Boolean</span></span>
<span data-ttu-id="c672e-129">이 cmdlet은 $True 또는 $False를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="c672e-130">작업이 성공적이 고 *PassThru* 매개 변수를 지정 하면이 cmdlet은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c672e-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="c672e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c672e-131">NOTES</span></span>

## <span data-ttu-id="c672e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c672e-132">RELATED LINKS</span></span>

[<span data-ttu-id="c672e-133">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c672e-133">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c672e-134">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c672e-134">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c672e-135">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c672e-135">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c672e-136">새로운 AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c672e-136">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c672e-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c672e-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


