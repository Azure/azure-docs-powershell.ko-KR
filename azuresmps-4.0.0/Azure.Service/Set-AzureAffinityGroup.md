---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046431"
---
# <span data-ttu-id="3d6f0-101">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="3d6f0-101">Set-AzureAffinityGroup</span></span>

## <span data-ttu-id="3d6f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d6f0-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6f0-103">선호도 그룹의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-103">Modifies properties of an affinity group.</span></span>

## <span data-ttu-id="3d6f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d6f0-104">SYNTAX</span></span>

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3d6f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3d6f0-105">DESCRIPTION</span></span>
<span data-ttu-id="3d6f0-106">**Set-AzureAffinityGroup** Cmdlet은 Azure 선호도 그룹의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-106">The **Set-AzureAffinityGroup** cmdlet modifies properties of an Azure affinity group.</span></span>
<span data-ttu-id="3d6f0-107">레이블과 설명을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-107">You can change the label and the description.</span></span>

## <span data-ttu-id="3d6f0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="3d6f0-108">EXAMPLES</span></span>

### <span data-ttu-id="3d6f0-109">예제 1: 선호도 그룹 수정</span><span class="sxs-lookup"><span data-stu-id="3d6f0-109">Example 1: Modify an affinity group</span></span>
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

<span data-ttu-id="3d6f0-110">이 명령은 South01 이라는 선호도 그룹의 레이블을 SouthUSProduction에 맞게 수정 하 여 설명도 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-110">This command modifies the label of the affinity group named South01 to be SouthUSProduction The command also modifies the description.</span></span>

## <span data-ttu-id="3d6f0-111">변수</span><span class="sxs-lookup"><span data-stu-id="3d6f0-111">PARAMETERS</span></span>

### <span data-ttu-id="3d6f0-112">-설명</span><span class="sxs-lookup"><span data-stu-id="3d6f0-112">-Description</span></span>
<span data-ttu-id="3d6f0-113">선호도 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-113">Specifies the description of the affinity group.</span></span>
<span data-ttu-id="3d6f0-114">설명은 최대 1024 자까지 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-114">The description can be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6f0-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3d6f0-115">-InformationAction</span></span>
<span data-ttu-id="3d6f0-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3d6f0-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d6f0-118">하기로</span><span class="sxs-lookup"><span data-stu-id="3d6f0-118">Continue</span></span>
- <span data-ttu-id="3d6f0-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="3d6f0-119">Ignore</span></span>
- <span data-ttu-id="3d6f0-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="3d6f0-120">Inquire</span></span>
- <span data-ttu-id="3d6f0-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3d6f0-121">SilentlyContinue</span></span>
- <span data-ttu-id="3d6f0-122">중지가</span><span class="sxs-lookup"><span data-stu-id="3d6f0-122">Stop</span></span>
- <span data-ttu-id="3d6f0-123">대기</span><span class="sxs-lookup"><span data-stu-id="3d6f0-123">Suspend</span></span>

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

### <span data-ttu-id="3d6f0-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3d6f0-124">-InformationVariable</span></span>
<span data-ttu-id="3d6f0-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3d6f0-126">-레이블</span><span class="sxs-lookup"><span data-stu-id="3d6f0-126">-Label</span></span>
<span data-ttu-id="3d6f0-127">선호도 그룹의 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-127">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="3d6f0-128">레이블 길이는 최대 100 자까지 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-128">The label can be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6f0-129">-이름</span><span class="sxs-lookup"><span data-stu-id="3d6f0-129">-Name</span></span>
<span data-ttu-id="3d6f0-130">이 cmdlet이 수정 하는 선호도 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-130">Specifies the name of the affinity group that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6f0-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="3d6f0-131">-Profile</span></span>
<span data-ttu-id="3d6f0-132">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d6f0-133">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d6f0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6f0-134">CommonParameters</span></span>
<span data-ttu-id="3d6f0-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d6f0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6f0-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6f0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6f0-137">입력</span><span class="sxs-lookup"><span data-stu-id="3d6f0-137">INPUTS</span></span>

## <span data-ttu-id="3d6f0-138">출력</span><span class="sxs-lookup"><span data-stu-id="3d6f0-138">OUTPUTS</span></span>

## <span data-ttu-id="3d6f0-139">상속자</span><span class="sxs-lookup"><span data-stu-id="3d6f0-139">NOTES</span></span>

## <span data-ttu-id="3d6f0-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d6f0-140">RELATED LINKS</span></span>

[<span data-ttu-id="3d6f0-141">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="3d6f0-141">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="3d6f0-142">새로운 AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="3d6f0-142">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="3d6f0-143">제거-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="3d6f0-143">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)


