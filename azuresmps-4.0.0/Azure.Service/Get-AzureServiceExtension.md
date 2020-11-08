---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2664607C-FF95-4EB7-869E-A421343B0517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 231f24a20471d8a4639b091c10d0e04f65b71b76
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045599"
---
# <span data-ttu-id="ba5b0-101">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="ba5b0-101">Get-AzureServiceExtension</span></span>

## <span data-ttu-id="ba5b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5b0-103">배포에 적용 되는 클라우드 서비스 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-103">Gets cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="ba5b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba5b0-104">SYNTAX</span></span>

```
Get-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-ExtensionName] <String>]
 [[-ProviderNamespace] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ba5b0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba5b0-105">DESCRIPTION</span></span>
<span data-ttu-id="ba5b0-106">**Get-AzureServiceExtension** cmdlet은 배포에 적용 되는 기존 클라우드 서비스 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-106">The **Get-AzureServiceExtension** cmdlet gets existing cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="ba5b0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ba5b0-107">EXAMPLES</span></span>

### <span data-ttu-id="ba5b0-108">예제 1: 지정 된 확장명 가져오기</span><span class="sxs-lookup"><span data-stu-id="ba5b0-108">Example 1: Get a specified extension</span></span>
```
PS C:\> Get-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="ba5b0-109">이 명령은 지정 된 이름 및 네임 스페이스를 사용 하 여 클라우드 서비스 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-109">This command gets the cloud service extension with the specified name and namespace.</span></span>

## <span data-ttu-id="ba5b0-110">변수</span><span class="sxs-lookup"><span data-stu-id="ba5b0-110">PARAMETERS</span></span>

### <span data-ttu-id="ba5b0-111">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="ba5b0-111">-ExtensionName</span></span>
<span data-ttu-id="ba5b0-112">확장명 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-112">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5b0-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ba5b0-113">-InformationAction</span></span>
<span data-ttu-id="ba5b0-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ba5b0-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba5b0-116">하기로</span><span class="sxs-lookup"><span data-stu-id="ba5b0-116">Continue</span></span>
- <span data-ttu-id="ba5b0-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="ba5b0-117">Ignore</span></span>
- <span data-ttu-id="ba5b0-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="ba5b0-118">Inquire</span></span>
- <span data-ttu-id="ba5b0-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ba5b0-119">SilentlyContinue</span></span>
- <span data-ttu-id="ba5b0-120">중지가</span><span class="sxs-lookup"><span data-stu-id="ba5b0-120">Stop</span></span>
- <span data-ttu-id="ba5b0-121">대기</span><span class="sxs-lookup"><span data-stu-id="ba5b0-121">Suspend</span></span>

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

### <span data-ttu-id="ba5b0-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ba5b0-122">-InformationVariable</span></span>
<span data-ttu-id="ba5b0-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ba5b0-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="ba5b0-124">-Profile</span></span>
<span data-ttu-id="ba5b0-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba5b0-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba5b0-127">ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ba5b0-127">-ProviderNamespace</span></span>
<span data-ttu-id="ba5b0-128">확장 공급자 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-128">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5b0-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ba5b0-129">-ServiceName</span></span>
<span data-ttu-id="ba5b0-130">배포의 Azure 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-130">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="ba5b0-131">-슬롯</span><span class="sxs-lookup"><span data-stu-id="ba5b0-131">-Slot</span></span>
<span data-ttu-id="ba5b0-132">배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-132">Specifies the deployment environment.</span></span>
<span data-ttu-id="ba5b0-133">이 매개 변수에 허용 되는 값은 프로덕션 또는 스테이징입니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-133">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="ba5b0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5b0-134">CommonParameters</span></span>
<span data-ttu-id="ba5b0-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5b0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5b0-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba5b0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5b0-137">입력</span><span class="sxs-lookup"><span data-stu-id="ba5b0-137">INPUTS</span></span>

## <span data-ttu-id="ba5b0-138">출력</span><span class="sxs-lookup"><span data-stu-id="ba5b0-138">OUTPUTS</span></span>

## <span data-ttu-id="ba5b0-139">상속자</span><span class="sxs-lookup"><span data-stu-id="ba5b0-139">NOTES</span></span>

## <span data-ttu-id="ba5b0-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba5b0-140">RELATED LINKS</span></span>

[<span data-ttu-id="ba5b0-141">-AzureServiceExtension 제거</span><span class="sxs-lookup"><span data-stu-id="ba5b0-141">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)

[<span data-ttu-id="ba5b0-142">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="ba5b0-142">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


