---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045637"
---
# <span data-ttu-id="32a22-101">Get-AzureOSVersion</span><span class="sxs-lookup"><span data-stu-id="32a22-101">Get-AzureOSVersion</span></span>

## <span data-ttu-id="32a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32a22-102">SYNOPSIS</span></span>
<span data-ttu-id="32a22-103">모든 Azure 게스트 운영 체제를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-103">Lists all Azure guest operating systems.</span></span>

## <span data-ttu-id="32a22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32a22-104">SYNTAX</span></span>

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="32a22-105">설명은</span><span class="sxs-lookup"><span data-stu-id="32a22-105">DESCRIPTION</span></span>
<span data-ttu-id="32a22-106">**Get-AzureOSVersion** cmdlet에는 사용 가능한 모든 Azure 게스트 운영 체제가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-106">The **Get-AzureOSVersion** cmdlet lists all the available Azure guest operating systems.</span></span>

## <span data-ttu-id="32a22-107">예제의</span><span class="sxs-lookup"><span data-stu-id="32a22-107">EXAMPLES</span></span>

### <span data-ttu-id="32a22-108">예제 1: 사용 가능한 모든 운영 체제 가져오기</span><span class="sxs-lookup"><span data-stu-id="32a22-108">Example 1: Get all available operating systems</span></span>
```
PS C:\> Get-AzureOSVersion
```

<span data-ttu-id="32a22-109">이 명령은 현재 구독에서 사용할 수 있는 모든 버전의 게스트 운영 체제 목록을 포함 하는 개체를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-109">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>

### <span data-ttu-id="32a22-110">예제 2: 표에 운영 체제 정보 표시</span><span class="sxs-lookup"><span data-stu-id="32a22-110">Example 2: Display operating system information in a table</span></span>
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

<span data-ttu-id="32a22-111">이 명령은 현재 구독에서 사용할 수 있는 모든 버전의 게스트 운영 체제 목록을 포함 하는 개체를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-111">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>
<span data-ttu-id="32a22-112">이 명령은 파이프라인 연산자를 사용 하 여이를 **형식 테이블** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-112">The command passes them to the **Format-Table** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="32a22-113">해당 cmdlet은 운영 체제 제품군, 운영 체제 패밀리 레이블 및 버전이 표시 되는 표로 서식 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-113">That cmdlet formats them as a table that shows the operating system family, operating system family label, and version.</span></span>

## <span data-ttu-id="32a22-114">변수</span><span class="sxs-lookup"><span data-stu-id="32a22-114">PARAMETERS</span></span>

### <span data-ttu-id="32a22-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="32a22-115">-InformationAction</span></span>
<span data-ttu-id="32a22-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="32a22-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="32a22-118">하기로</span><span class="sxs-lookup"><span data-stu-id="32a22-118">Continue</span></span>
- <span data-ttu-id="32a22-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="32a22-119">Ignore</span></span>
- <span data-ttu-id="32a22-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="32a22-120">Inquire</span></span>
- <span data-ttu-id="32a22-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="32a22-121">SilentlyContinue</span></span>
- <span data-ttu-id="32a22-122">중지가</span><span class="sxs-lookup"><span data-stu-id="32a22-122">Stop</span></span>
- <span data-ttu-id="32a22-123">대기</span><span class="sxs-lookup"><span data-stu-id="32a22-123">Suspend</span></span>

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

### <span data-ttu-id="32a22-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="32a22-124">-InformationVariable</span></span>
<span data-ttu-id="32a22-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="32a22-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="32a22-126">-Profile</span></span>
<span data-ttu-id="32a22-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32a22-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32a22-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a22-129">CommonParameters</span></span>
<span data-ttu-id="32a22-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32a22-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a22-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32a22-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a22-132">입력</span><span class="sxs-lookup"><span data-stu-id="32a22-132">INPUTS</span></span>

## <span data-ttu-id="32a22-133">출력</span><span class="sxs-lookup"><span data-stu-id="32a22-133">OUTPUTS</span></span>

## <span data-ttu-id="32a22-134">상속자</span><span class="sxs-lookup"><span data-stu-id="32a22-134">NOTES</span></span>

## <span data-ttu-id="32a22-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32a22-135">RELATED LINKS</span></span>

[<span data-ttu-id="32a22-136">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="32a22-136">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)


