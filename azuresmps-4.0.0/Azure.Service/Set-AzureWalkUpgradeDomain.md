---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F3BC5AF-8D7B-40BF-A072-A11C7BDCB6B3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09adc7e9b2faf9b9a905fa1c94fb6526e02c110f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045786"
---
# <span data-ttu-id="8a254-101">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="8a254-101">Set-AzureWalkUpgradeDomain</span></span>

## <span data-ttu-id="8a254-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a254-102">SYNOPSIS</span></span>
<span data-ttu-id="8a254-103">지정 된 업그레이드 도메인을 안내 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-103">Walks the specified upgrade domain.</span></span>

## <span data-ttu-id="8a254-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a254-104">SYNTAX</span></span>

```
Set-AzureWalkUpgradeDomain [-ServiceName] <String> [-Slot] <String> [-DomainNumber] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a254-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a254-105">DESCRIPTION</span></span>
<span data-ttu-id="8a254-106">**Set-AzureWalkUpgradeDomain** Cmdlet은 Azure 배포의 실제 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-106">The **Set-AzureWalkUpgradeDomain** cmdlet initiates the actual upgrade of an Azure deployment.</span></span>
<span data-ttu-id="8a254-107">업그레이드 패키지 및 구성은-Upgrade 스위치를 사용 하 여 **Set AzureDeployment** cmdlet을 사용 하 여 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-107">The upgrade package and configuration are set by using the **Set-AzureDeployment** cmdlet with the -Upgrade switch.</span></span>

## <span data-ttu-id="8a254-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8a254-108">EXAMPLES</span></span>

### <span data-ttu-id="8a254-109">예제 1: 프로덕션 배포의 업그레이드 시작</span><span class="sxs-lookup"><span data-stu-id="8a254-109">Example 1: Initiate an upgrade of a production deployment</span></span>
```
PS C:\> Set-AzureWalkUpgradeDomain -ServiceName "MySvc1" -slot "Production" -UpgradeDomain 2
```

<span data-ttu-id="8a254-110">이 명령은 MySvc1 서비스의 프로덕션 배포의 업그레이드 도메인 2 업그레이드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-110">This command initiates the upgrade of Upgrade Domain 2 of the production deployment of the MySvc1 service.</span></span>

## <span data-ttu-id="8a254-111">변수</span><span class="sxs-lookup"><span data-stu-id="8a254-111">PARAMETERS</span></span>

### <span data-ttu-id="8a254-112">-DomainNumber</span><span class="sxs-lookup"><span data-stu-id="8a254-112">-DomainNumber</span></span>
<span data-ttu-id="8a254-113">업그레이드할 업그레이드 도메인을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-113">Specifies the upgrade domain to upgrade.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a254-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8a254-114">-InformationAction</span></span>
<span data-ttu-id="8a254-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8a254-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a254-117">하기로</span><span class="sxs-lookup"><span data-stu-id="8a254-117">Continue</span></span>
- <span data-ttu-id="8a254-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="8a254-118">Ignore</span></span>
- <span data-ttu-id="8a254-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="8a254-119">Inquire</span></span>
- <span data-ttu-id="8a254-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a254-120">SilentlyContinue</span></span>
- <span data-ttu-id="8a254-121">중지가</span><span class="sxs-lookup"><span data-stu-id="8a254-121">Stop</span></span>
- <span data-ttu-id="8a254-122">대기</span><span class="sxs-lookup"><span data-stu-id="8a254-122">Suspend</span></span>

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

### <span data-ttu-id="8a254-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a254-123">-InformationVariable</span></span>
<span data-ttu-id="8a254-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8a254-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="8a254-125">-Profile</span></span>
<span data-ttu-id="8a254-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a254-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8a254-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8a254-128">-ServiceName</span></span>
<span data-ttu-id="8a254-129">업그레이드할 Microsoft Azure 서비스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-129">Specifies the Microsoft Azure service name to upgrade.</span></span>

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

### <span data-ttu-id="8a254-130">-슬롯</span><span class="sxs-lookup"><span data-stu-id="8a254-130">-Slot</span></span>
<span data-ttu-id="8a254-131">업그레이드할 배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-131">Specifies the environment of the deployment to upgrade.</span></span>

<span data-ttu-id="8a254-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a254-133">대기</span><span class="sxs-lookup"><span data-stu-id="8a254-133">Staging</span></span>
- <span data-ttu-id="8a254-134">프로덕션용</span><span class="sxs-lookup"><span data-stu-id="8a254-134">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a254-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a254-135">CommonParameters</span></span>
<span data-ttu-id="8a254-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a254-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a254-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a254-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a254-138">입력</span><span class="sxs-lookup"><span data-stu-id="8a254-138">INPUTS</span></span>

## <span data-ttu-id="8a254-139">출력</span><span class="sxs-lookup"><span data-stu-id="8a254-139">OUTPUTS</span></span>

### <span data-ttu-id="8a254-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="8a254-140">ManagementOperationContext</span></span>

## <span data-ttu-id="8a254-141">상속자</span><span class="sxs-lookup"><span data-stu-id="8a254-141">NOTES</span></span>

## <span data-ttu-id="8a254-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a254-142">RELATED LINKS</span></span>

[<span data-ttu-id="8a254-143">Set AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8a254-143">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


