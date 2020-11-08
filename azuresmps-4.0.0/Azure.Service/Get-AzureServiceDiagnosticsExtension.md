---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 235DD5D7-BE24-4FBE-88E2-40D1943ED155
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4fb3f35bc64a1431550d4da5aa669e934cd3a7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045603"
---
# <span data-ttu-id="5887d-101">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5887d-101">Get-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="5887d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5887d-102">SYNOPSIS</span></span>
<span data-ttu-id="5887d-103">특정 배포 슬롯의 모든 역할 또는 명명 된 역할에 적용 되는 클라우드 서비스 진단 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-103">Gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="5887d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5887d-104">SYNTAX</span></span>

```
Get-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5887d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5887d-105">DESCRIPTION</span></span>
<span data-ttu-id="5887d-106">**AzureServiceDiagnosticsExtension** cmdlet은 특정 배포 슬롯의 모든 역할 또는 명명 된 역할에 적용 되는 클라우드 서비스 진단 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-106">The **Get-AzureServiceDiagnosticsExtension** cmdlet gets the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="5887d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5887d-107">EXAMPLES</span></span>

### <span data-ttu-id="5887d-108">예제 1: 서비스 진단 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="5887d-108">Example 1: Get service diagnostics extension</span></span> 
```
PS C:\> Get-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="5887d-109">이 명령은 모든 역할에 걸친 서비스에 대 한 서비스 진단을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-109">This command gets the service diagnostics for a service, across all roles.</span></span>

## <span data-ttu-id="5887d-110">변수</span><span class="sxs-lookup"><span data-stu-id="5887d-110">PARAMETERS</span></span>

### <span data-ttu-id="5887d-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5887d-111">-InformationAction</span></span>
<span data-ttu-id="5887d-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5887d-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5887d-114">하기로</span><span class="sxs-lookup"><span data-stu-id="5887d-114">Continue</span></span>
- <span data-ttu-id="5887d-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="5887d-115">Ignore</span></span>
- <span data-ttu-id="5887d-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="5887d-116">Inquire</span></span>
- <span data-ttu-id="5887d-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5887d-117">SilentlyContinue</span></span>
- <span data-ttu-id="5887d-118">중지가</span><span class="sxs-lookup"><span data-stu-id="5887d-118">Stop</span></span>
- <span data-ttu-id="5887d-119">대기</span><span class="sxs-lookup"><span data-stu-id="5887d-119">Suspend</span></span>

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

### <span data-ttu-id="5887d-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5887d-120">-InformationVariable</span></span>
<span data-ttu-id="5887d-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5887d-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="5887d-122">-Profile</span></span>
<span data-ttu-id="5887d-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5887d-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5887d-125">-역할</span><span class="sxs-lookup"><span data-stu-id="5887d-125">-Role</span></span>
<span data-ttu-id="5887d-126">역할의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-126">Specifies an array of roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5887d-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5887d-127">-ServiceName</span></span>
<span data-ttu-id="5887d-128">배포의 Azure 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-128">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="5887d-129">-슬롯</span><span class="sxs-lookup"><span data-stu-id="5887d-129">-Slot</span></span>
<span data-ttu-id="5887d-130">수정할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-130">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="5887d-131">이 매개 변수에 허용 되는 값은 프로덕션 또는 스테이징입니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-131">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="5887d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5887d-132">CommonParameters</span></span>
<span data-ttu-id="5887d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5887d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5887d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5887d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5887d-135">입력</span><span class="sxs-lookup"><span data-stu-id="5887d-135">INPUTS</span></span>

## <span data-ttu-id="5887d-136">출력</span><span class="sxs-lookup"><span data-stu-id="5887d-136">OUTPUTS</span></span>

## <span data-ttu-id="5887d-137">상속자</span><span class="sxs-lookup"><span data-stu-id="5887d-137">NOTES</span></span>

## <span data-ttu-id="5887d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5887d-138">RELATED LINKS</span></span>

[<span data-ttu-id="5887d-139">제거-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5887d-139">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="5887d-140">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5887d-140">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


