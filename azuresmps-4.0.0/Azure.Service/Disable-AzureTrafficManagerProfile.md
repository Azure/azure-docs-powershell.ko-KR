---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045693"
---
# <span data-ttu-id="85bcc-101">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="85bcc-101">Disable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="85bcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="85bcc-103">Traffic Manager 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="85bcc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85bcc-104">SYNTAX</span></span>

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="85bcc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="85bcc-105">DESCRIPTION</span></span>
<span data-ttu-id="85bcc-106">**AzureTrafficManagerProfile** Cmdlet은 Microsoft Azure Traffic Manager 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-106">The **Disable-AzureTrafficManagerProfile** cmdlet disables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="85bcc-107">*PassThru* 매개 변수를 사용 하 여 작업 성공 여부를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-107">You can use the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="85bcc-108">예제의</span><span class="sxs-lookup"><span data-stu-id="85bcc-108">EXAMPLES</span></span>

### <span data-ttu-id="85bcc-109">예제 1: Traffic Manager 프로필을 사용 하지 않도록 설정 하 고 결과 표시</span><span class="sxs-lookup"><span data-stu-id="85bcc-109">Example 1: Disable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="85bcc-110">이 명령은 MyProfile 이라는 Traffic Manager 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-110">This command disables the Traffic Manager profile named MyProfile.</span></span>
<span data-ttu-id="85bcc-111">명령이 성공 했는지 여부를 표시 하는 *PassThru* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-111">The command specifies the *PassThru* parameter to display whether the command succeeded.</span></span>

### <span data-ttu-id="85bcc-112">예제 2: Traffic Manager 프로필을 비활성화 하 고 결과를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-112">Example 2: Disable a Traffic Manager profile and display no results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="85bcc-113">이 명령은 MyProfile 이라는 Traffic Manager 프로필을 사용 하지 않도록 설정 하지만 명령의 성공 여부는 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-113">This command disables the Traffic Manager profile named MyProfile but does not display whether the command succeeded.</span></span>

## <span data-ttu-id="85bcc-114">변수</span><span class="sxs-lookup"><span data-stu-id="85bcc-114">PARAMETERS</span></span>

### <span data-ttu-id="85bcc-115">-이름</span><span class="sxs-lookup"><span data-stu-id="85bcc-115">-Name</span></span>
<span data-ttu-id="85bcc-116">사용 하지 않도록 설정할 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-116">Specifies the name of the Traffic Manager profile to disable.</span></span>

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

### <span data-ttu-id="85bcc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85bcc-117">-PassThru</span></span>
<span data-ttu-id="85bcc-118">작업이 성공한 경우 $True를 반환 하 고, 그렇지 않으면 그렇지 않으면 $False 합니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="85bcc-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="85bcc-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="85bcc-120">-Profile</span></span>
<span data-ttu-id="85bcc-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="85bcc-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="85bcc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85bcc-123">CommonParameters</span></span>
<span data-ttu-id="85bcc-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85bcc-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85bcc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85bcc-126">입력</span><span class="sxs-lookup"><span data-stu-id="85bcc-126">INPUTS</span></span>

## <span data-ttu-id="85bcc-127">출력</span><span class="sxs-lookup"><span data-stu-id="85bcc-127">OUTPUTS</span></span>

### <span data-ttu-id="85bcc-128">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="85bcc-128">System.Boolean</span></span>
<span data-ttu-id="85bcc-129">이 cmdlet은 $True 또는 $False를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="85bcc-130">작업이 성공적이 고 *PassThru* 매개 변수를 지정 하면이 cmdlet은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="85bcc-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="85bcc-131">상속자</span><span class="sxs-lookup"><span data-stu-id="85bcc-131">NOTES</span></span>

## <span data-ttu-id="85bcc-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85bcc-132">RELATED LINKS</span></span>

[<span data-ttu-id="85bcc-133">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="85bcc-133">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="85bcc-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="85bcc-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="85bcc-135">새로운 AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="85bcc-135">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="85bcc-136">제거-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="85bcc-136">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="85bcc-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="85bcc-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


