---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 761317FE-55FD-4DCC-B997-4F27D041470F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77f58c4f3ee1c440e35c43648f92d21793efddc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046145"
---
# <span data-ttu-id="0f56d-101">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="0f56d-101">Remove-AzureReservedIP</span></span>

## <span data-ttu-id="0f56d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f56d-102">SYNOPSIS</span></span>
<span data-ttu-id="0f56d-103">예약 된 IP 주소를 이름으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-103">Removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="0f56d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f56d-104">SYNTAX</span></span>

```
Remove-AzureReservedIP [-ReservedIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0f56d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0f56d-105">DESCRIPTION</span></span>
<span data-ttu-id="0f56d-106">**AzureReservedIP** cmdlet은 이름으로 예약 된 IP 주소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-106">The **Remove-AzureReservedIP** cmdlet removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="0f56d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0f56d-107">EXAMPLES</span></span>

### <span data-ttu-id="0f56d-108">예제 1: 이름으로 예약 된 IP 주소 제거</span><span class="sxs-lookup"><span data-stu-id="0f56d-108">Example 1: Remove a reserved IP address by its name</span></span>
```
PS C:\> Remove-AzureReservedIP -ReservedIPName $name
```

<span data-ttu-id="0f56d-109">이 명령은 예약 된 IP 주소를 이름으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-109">This command removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="0f56d-110">변수</span><span class="sxs-lookup"><span data-stu-id="0f56d-110">PARAMETERS</span></span>

### <span data-ttu-id="0f56d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0f56d-111">-Force</span></span>
<span data-ttu-id="0f56d-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f56d-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0f56d-113">-InformationAction</span></span>
<span data-ttu-id="0f56d-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0f56d-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f56d-116">하기로</span><span class="sxs-lookup"><span data-stu-id="0f56d-116">Continue</span></span>
- <span data-ttu-id="0f56d-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="0f56d-117">Ignore</span></span>
- <span data-ttu-id="0f56d-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="0f56d-118">Inquire</span></span>
- <span data-ttu-id="0f56d-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0f56d-119">SilentlyContinue</span></span>
- <span data-ttu-id="0f56d-120">중지가</span><span class="sxs-lookup"><span data-stu-id="0f56d-120">Stop</span></span>
- <span data-ttu-id="0f56d-121">대기</span><span class="sxs-lookup"><span data-stu-id="0f56d-121">Suspend</span></span>

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

### <span data-ttu-id="0f56d-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0f56d-122">-InformationVariable</span></span>
<span data-ttu-id="0f56d-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0f56d-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="0f56d-124">-Profile</span></span>
<span data-ttu-id="0f56d-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f56d-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f56d-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="0f56d-127">-ReservedIPName</span></span>
<span data-ttu-id="0f56d-128">예약 된 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-128">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="0f56d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f56d-129">CommonParameters</span></span>
<span data-ttu-id="0f56d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f56d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f56d-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f56d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f56d-132">입력</span><span class="sxs-lookup"><span data-stu-id="0f56d-132">INPUTS</span></span>

## <span data-ttu-id="0f56d-133">출력</span><span class="sxs-lookup"><span data-stu-id="0f56d-133">OUTPUTS</span></span>

## <span data-ttu-id="0f56d-134">상속자</span><span class="sxs-lookup"><span data-stu-id="0f56d-134">NOTES</span></span>

## <span data-ttu-id="0f56d-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f56d-135">RELATED LINKS</span></span>

[<span data-ttu-id="0f56d-136">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="0f56d-136">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="0f56d-137">새로운 AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="0f56d-137">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="0f56d-138">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="0f56d-138">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


