---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046244"
---
# <span data-ttu-id="4632a-101">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4632a-101">Move-AzureDeployment</span></span>

## <span data-ttu-id="4632a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4632a-102">SYNOPSIS</span></span>
<span data-ttu-id="4632a-103">프로덕션 및 스테이징 간에 배포를 교환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-103">Swaps deployments between production and staging.</span></span>

## <span data-ttu-id="4632a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4632a-104">SYNTAX</span></span>

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4632a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4632a-105">DESCRIPTION</span></span>
<span data-ttu-id="4632a-106">**AzureDeployment Move** cmdlet은 프로덕션 및 스테이징 환경에서 배포의 가상 IP 주소를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-106">The **Move-AzureDeployment** cmdlet swaps the virtual IP addresses of deployments in production and staging environments.</span></span>
<span data-ttu-id="4632a-107">이 cmdlet은 스테이징 환경에서 현재 실행 되는 배포를 프로덕션 환경에 교환 하 고 프로덕션 환경에서 스테이징 환경으로 실행 하는 배포를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-107">This cmdlet swaps a deployment that currently runs in the staging environment to the production environment, and a deployment that runs in the production environment to the staging environment.</span></span>
<span data-ttu-id="4632a-108">스테이징 환경에 배포가 있고 프로덕션 환경에 배포 되지 않은 경우 cmdlet은 배포를 프로덕션으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-108">If there is a deployment in the staging environment and no deployment in the production environment, the cmdlet moves the deployment to production.</span></span>
<span data-ttu-id="4632a-109">프로덕션 환경에 배포가 있고 스테이징 환경에 배포 되지 않은 경우에는 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-109">If there is a deployment in the production environment and no deployment in the staging environment, the cmdlet fails.</span></span>

## <span data-ttu-id="4632a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4632a-110">EXAMPLES</span></span>

### <span data-ttu-id="4632a-111">예제 1: 서비스의 배포 교환</span><span class="sxs-lookup"><span data-stu-id="4632a-111">Example 1: Swap deployments for a service</span></span>
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="4632a-112">이 명령은 프로덕션 환경과 스테이징 환경 간에 ContosoService 이라는 서비스의 배포를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-112">This command swaps the deployments of the service named ContosoService between the production and staging environments.</span></span>

## <span data-ttu-id="4632a-113">변수</span><span class="sxs-lookup"><span data-stu-id="4632a-113">PARAMETERS</span></span>

### <span data-ttu-id="4632a-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4632a-114">-InformationAction</span></span>
<span data-ttu-id="4632a-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4632a-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4632a-117">하기로</span><span class="sxs-lookup"><span data-stu-id="4632a-117">Continue</span></span>
- <span data-ttu-id="4632a-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="4632a-118">Ignore</span></span>
- <span data-ttu-id="4632a-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="4632a-119">Inquire</span></span>
- <span data-ttu-id="4632a-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4632a-120">SilentlyContinue</span></span>
- <span data-ttu-id="4632a-121">중지가</span><span class="sxs-lookup"><span data-stu-id="4632a-121">Stop</span></span>
- <span data-ttu-id="4632a-122">대기</span><span class="sxs-lookup"><span data-stu-id="4632a-122">Suspend</span></span>

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

### <span data-ttu-id="4632a-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4632a-123">-InformationVariable</span></span>
<span data-ttu-id="4632a-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4632a-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="4632a-125">-Profile</span></span>
<span data-ttu-id="4632a-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4632a-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4632a-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4632a-128">-ServiceName</span></span>
<span data-ttu-id="4632a-129">이 cmdlet이 프로덕션 및 스테이징 배포를 바꾸는 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-129">Specifies the name of the service for which this cmdlet swaps production and staging deployments.</span></span>

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

### <span data-ttu-id="4632a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4632a-130">CommonParameters</span></span>
<span data-ttu-id="4632a-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4632a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4632a-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4632a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4632a-133">입력</span><span class="sxs-lookup"><span data-stu-id="4632a-133">INPUTS</span></span>

## <span data-ttu-id="4632a-134">출력</span><span class="sxs-lookup"><span data-stu-id="4632a-134">OUTPUTS</span></span>

### <span data-ttu-id="4632a-135">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="4632a-135">ManagementOperationContext</span></span>

## <span data-ttu-id="4632a-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4632a-136">NOTES</span></span>

## <span data-ttu-id="4632a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4632a-137">RELATED LINKS</span></span>

[<span data-ttu-id="4632a-138">다운로드-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4632a-138">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="4632a-139">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="4632a-139">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="4632a-140">새 AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4632a-140">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="4632a-141">-AzureDeployment 제거</span><span class="sxs-lookup"><span data-stu-id="4632a-141">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="4632a-142">Set AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="4632a-142">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


