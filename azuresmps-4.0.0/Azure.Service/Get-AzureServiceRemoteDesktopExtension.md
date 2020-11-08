---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D08CB0A0-A0A9-4E0A-B1AB-A19A655B501B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5fd66813dcfc08f5e2f5276c4019443f9166945d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045596"
---
# <span data-ttu-id="f82b3-101">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="f82b3-101">Get-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="f82b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f82b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f82b3-103">이 cmdlet은 특정 배포 슬롯의 모든 역할 또는 명명 된 역할에 적용 된 클라우드 서비스 원격 데스크톱 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-103">This cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="f82b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f82b3-104">SYNTAX</span></span>

```
Get-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f82b3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f82b3-105">DESCRIPTION</span></span>
<span data-ttu-id="f82b3-106">**Get-AzureServiceRemoteDesktopExtension** cmdlet은 특정 배포 슬롯의 모든 역할 또는 명명 된 역할에 적용 되는 클라우드 서비스 원격 데스크톱 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-106">The **Get-AzureServiceRemoteDesktopExtension** cmdlet gets the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="f82b3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f82b3-107">EXAMPLES</span></span>

### <span data-ttu-id="f82b3-108">예제 1: 지정 된 서비스에 대 한 원격 데스크톱 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="f82b3-108">Example 1: Get remote desktop extension for the specified service</span></span>
```
PS C:\> Get-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="f82b3-109">이 명령은 지정 된 서비스에 대 한 원격 데스크톱 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-109">This command gets the remote desktop extension for the specified service.</span></span>

## <span data-ttu-id="f82b3-110">변수</span><span class="sxs-lookup"><span data-stu-id="f82b3-110">PARAMETERS</span></span>

### <span data-ttu-id="f82b3-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f82b3-111">-InformationAction</span></span>
<span data-ttu-id="f82b3-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f82b3-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f82b3-114">하기로</span><span class="sxs-lookup"><span data-stu-id="f82b3-114">Continue</span></span>
- <span data-ttu-id="f82b3-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="f82b3-115">Ignore</span></span>
- <span data-ttu-id="f82b3-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="f82b3-116">Inquire</span></span>
- <span data-ttu-id="f82b3-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f82b3-117">SilentlyContinue</span></span>
- <span data-ttu-id="f82b3-118">중지가</span><span class="sxs-lookup"><span data-stu-id="f82b3-118">Stop</span></span>
- <span data-ttu-id="f82b3-119">대기</span><span class="sxs-lookup"><span data-stu-id="f82b3-119">Suspend</span></span>

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

### <span data-ttu-id="f82b3-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f82b3-120">-InformationVariable</span></span>
<span data-ttu-id="f82b3-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f82b3-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="f82b3-122">-Profile</span></span>
<span data-ttu-id="f82b3-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f82b3-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f82b3-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f82b3-125">-ServiceName</span></span>
<span data-ttu-id="f82b3-126">배포의 Azure 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-126">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="f82b3-127">-슬롯</span><span class="sxs-lookup"><span data-stu-id="f82b3-127">-Slot</span></span>
<span data-ttu-id="f82b3-128">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-128">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="f82b3-129">이 매개 변수에 허용 되는 값은 프로덕션 또는 스테이징입니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-129">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f82b3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f82b3-130">CommonParameters</span></span>
<span data-ttu-id="f82b3-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f82b3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f82b3-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f82b3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f82b3-133">입력</span><span class="sxs-lookup"><span data-stu-id="f82b3-133">INPUTS</span></span>

## <span data-ttu-id="f82b3-134">출력</span><span class="sxs-lookup"><span data-stu-id="f82b3-134">OUTPUTS</span></span>

## <span data-ttu-id="f82b3-135">상속자</span><span class="sxs-lookup"><span data-stu-id="f82b3-135">NOTES</span></span>

## <span data-ttu-id="f82b3-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f82b3-136">RELATED LINKS</span></span>

[<span data-ttu-id="f82b3-137">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="f82b3-137">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


