---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 77B26360-F22B-457F-BDE3-9920A5736947
online version: ''
schema: 2.0.0
ms.openlocfilehash: 323b04a57cffc71059dff3f91480d54684941695
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045671"
---
# <span data-ttu-id="9f032-101">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="9f032-101">Get-AzureAffinityGroup</span></span>

## <span data-ttu-id="9f032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f032-102">SYNOPSIS</span></span>
<span data-ttu-id="9f032-103">Azure 선호도 그룹 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-103">Gets an Azure affinity group object.</span></span>

## <span data-ttu-id="9f032-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f032-104">SYNTAX</span></span>

```
Get-AzureAffinityGroup [[-Name] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9f032-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9f032-105">DESCRIPTION</span></span>
<span data-ttu-id="9f032-106">**Get-AzureAffinityGroup** Cmdlet은 Azure 선호도 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-106">The **Get-AzureAffinityGroup** cmdlet gets an Azure affinity group.</span></span>
<span data-ttu-id="9f032-107">Affinity group 개체에는 선호도 그룹 이름, 위치, 레이블, 설명, 선호도 그룹의 일부인 저장소 및 호스트 된 서비스가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-107">The affinity group object includes the affinity group name, location, label, description and the storage and hosted services that are part of the affinity group.</span></span>

## <span data-ttu-id="9f032-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9f032-108">EXAMPLES</span></span>

### <span data-ttu-id="9f032-109">예제 1: 선호도 그룹의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="9f032-109">Example 1: Get properties of an affinity group</span></span>
```
PS C:\> Get-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="9f032-110">이 명령은 South01 이라는 선호도 그룹의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-110">This command gets the properties of the affinity group named South01.</span></span>

## <span data-ttu-id="9f032-111">변수</span><span class="sxs-lookup"><span data-stu-id="9f032-111">PARAMETERS</span></span>

### <span data-ttu-id="9f032-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9f032-112">-InformationAction</span></span>
<span data-ttu-id="9f032-113">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9f032-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f032-115">하기로</span><span class="sxs-lookup"><span data-stu-id="9f032-115">Continue</span></span>
- <span data-ttu-id="9f032-116">숨기기</span><span class="sxs-lookup"><span data-stu-id="9f032-116">Ignore</span></span>
- <span data-ttu-id="9f032-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="9f032-117">Inquire</span></span>
- <span data-ttu-id="9f032-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9f032-118">SilentlyContinue</span></span>
- <span data-ttu-id="9f032-119">중지가</span><span class="sxs-lookup"><span data-stu-id="9f032-119">Stop</span></span>
- <span data-ttu-id="9f032-120">대기</span><span class="sxs-lookup"><span data-stu-id="9f032-120">Suspend</span></span>

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

### <span data-ttu-id="9f032-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9f032-121">-InformationVariable</span></span>
<span data-ttu-id="9f032-122">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9f032-123">-이름</span><span class="sxs-lookup"><span data-stu-id="9f032-123">-Name</span></span>
<span data-ttu-id="9f032-124">이 cmdlet이 가져오는 선호도 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-124">Specifies the name of the affinity group that this cmdlet gets.</span></span>
<span data-ttu-id="9f032-125">관리 포털을 통해 생성 된 선호도 그룹의 이름은 일반적으로 Guid입니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-125">Names for affinity groups created through the Management Portal are typically GUIDs.</span></span>
<span data-ttu-id="9f032-126">관리 포트는 선호도 그룹 레이블을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-126">The Management Port shows the affinity group label.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f032-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="9f032-127">-Profile</span></span>
<span data-ttu-id="9f032-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9f032-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9f032-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f032-130">CommonParameters</span></span>
<span data-ttu-id="9f032-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f032-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f032-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f032-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f032-133">입력</span><span class="sxs-lookup"><span data-stu-id="9f032-133">INPUTS</span></span>

## <span data-ttu-id="9f032-134">출력</span><span class="sxs-lookup"><span data-stu-id="9f032-134">OUTPUTS</span></span>

### <span data-ttu-id="9f032-135">AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="9f032-135">AffinityGroup</span></span>

## <span data-ttu-id="9f032-136">상속자</span><span class="sxs-lookup"><span data-stu-id="9f032-136">NOTES</span></span>

## <span data-ttu-id="9f032-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f032-137">RELATED LINKS</span></span>

[<span data-ttu-id="9f032-138">새로운 AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="9f032-138">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="9f032-139">제거-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="9f032-139">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="9f032-140">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="9f032-140">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


