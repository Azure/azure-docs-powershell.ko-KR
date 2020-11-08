---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 29602F63-A05B-45AF-8DD8-5EBBF4C33FCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32af8d2e89c14b0d36265efc688a88858851bba5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046172"
---
# <span data-ttu-id="5af2d-101">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="5af2d-101">Remove-AzureAffinityGroup</span></span>

## <span data-ttu-id="5af2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5af2d-102">SYNOPSIS</span></span>
<span data-ttu-id="5af2d-103">구독에서 선호도 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-103">Deletes an affinity group in a subscription.</span></span>

## <span data-ttu-id="5af2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5af2d-104">SYNTAX</span></span>

```
Remove-AzureAffinityGroup [-Name] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5af2d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5af2d-105">DESCRIPTION</span></span>
<span data-ttu-id="5af2d-106">**AzureAffinityGroup** cmdlet은 현재 구독에서 Azure 선호도 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-106">The **Remove-AzureAffinityGroup** cmdlet deletes an Azure affinity group in the current subscription.</span></span>
<span data-ttu-id="5af2d-107">구성원이 있는 선호도 그룹은 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-107">You cannot delete an affinity group that has any members.</span></span>
<span data-ttu-id="5af2d-108">먼저 선호도 그룹의 모든 구성원을 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-108">You must first delete all the members of an affinity group.</span></span>

## <span data-ttu-id="5af2d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5af2d-109">EXAMPLES</span></span>

### <span data-ttu-id="5af2d-110">예제 1: 선호도 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="5af2d-110">Example 1: Remove an affinity group</span></span>
```
PS C:\> Remove-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="5af2d-111">이 명령은 현재 구독에서 South01 affinity 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-111">This command deletes the South01 affinity group in the current subscription.</span></span>

## <span data-ttu-id="5af2d-112">변수</span><span class="sxs-lookup"><span data-stu-id="5af2d-112">PARAMETERS</span></span>

### <span data-ttu-id="5af2d-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5af2d-113">-InformationAction</span></span>
<span data-ttu-id="5af2d-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5af2d-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5af2d-116">하기로</span><span class="sxs-lookup"><span data-stu-id="5af2d-116">Continue</span></span>
- <span data-ttu-id="5af2d-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="5af2d-117">Ignore</span></span>
- <span data-ttu-id="5af2d-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="5af2d-118">Inquire</span></span>
- <span data-ttu-id="5af2d-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5af2d-119">SilentlyContinue</span></span>
- <span data-ttu-id="5af2d-120">중지가</span><span class="sxs-lookup"><span data-stu-id="5af2d-120">Stop</span></span>
- <span data-ttu-id="5af2d-121">대기</span><span class="sxs-lookup"><span data-stu-id="5af2d-121">Suspend</span></span>

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

### <span data-ttu-id="5af2d-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5af2d-122">-InformationVariable</span></span>
<span data-ttu-id="5af2d-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5af2d-124">-이름</span><span class="sxs-lookup"><span data-stu-id="5af2d-124">-Name</span></span>
<span data-ttu-id="5af2d-125">이 cmdlet이 삭제 하는 선호도 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-125">Specifies the name of the affinity group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="5af2d-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="5af2d-126">-Profile</span></span>
<span data-ttu-id="5af2d-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5af2d-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5af2d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af2d-129">CommonParameters</span></span>
<span data-ttu-id="5af2d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5af2d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af2d-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af2d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af2d-132">입력</span><span class="sxs-lookup"><span data-stu-id="5af2d-132">INPUTS</span></span>

## <span data-ttu-id="5af2d-133">출력</span><span class="sxs-lookup"><span data-stu-id="5af2d-133">OUTPUTS</span></span>

## <span data-ttu-id="5af2d-134">상속자</span><span class="sxs-lookup"><span data-stu-id="5af2d-134">NOTES</span></span>

## <span data-ttu-id="5af2d-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5af2d-135">RELATED LINKS</span></span>

[<span data-ttu-id="5af2d-136">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="5af2d-136">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="5af2d-137">새로운 AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="5af2d-137">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="5af2d-138">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="5af2d-138">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


