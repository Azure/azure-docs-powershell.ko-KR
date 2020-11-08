---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046355"
---
# <span data-ttu-id="1dd2f-101">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="1dd2f-101">Get-AzureDeployment</span></span>

## <span data-ttu-id="1dd2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dd2f-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd2f-103">배포에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-103">Gets details of a deployment.</span></span>

## <span data-ttu-id="1dd2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1dd2f-104">SYNTAX</span></span>

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1dd2f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1dd2f-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd2f-106">**가져오기-azuredeployment** Cmdlet은 Azure 배포의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-106">The **Get-AzureDeployment** cmdlet gets details of an Azure deployment.</span></span>
<span data-ttu-id="1dd2f-107">Azure 서비스의 이름과 배포 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-107">Specify the name of the Azure service and the slot of the deployment.</span></span>

## <span data-ttu-id="1dd2f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1dd2f-108">EXAMPLES</span></span>

### <span data-ttu-id="1dd2f-109">예제 1: 프로덕션 배포에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="1dd2f-109">Example 1: Get details for a production deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="1dd2f-110">이 명령은 ContosoService 이라는 서비스에 대 한 배포 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-110">This command returns the details of the deployment for the service named ContosoService.</span></span>
<span data-ttu-id="1dd2f-111">이 명령은 슬롯을 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-111">This command does not specify a slot.</span></span>
<span data-ttu-id="1dd2f-112">따라서이 명령은 기본 프로덕션 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-112">Therefore, the command uses the default value of Production.</span></span>

### <span data-ttu-id="1dd2f-113">예제 2: 스테이징 배포에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="1dd2f-113">Example 2: Get details for a staging deployment</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

<span data-ttu-id="1dd2f-114">이 명령은 ContosoService의 스테이징 배포에 대 한 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-114">This command returns the details of the staging deployment of ContosoService.</span></span>

## <span data-ttu-id="1dd2f-115">변수</span><span class="sxs-lookup"><span data-stu-id="1dd2f-115">PARAMETERS</span></span>

### <span data-ttu-id="1dd2f-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1dd2f-116">-InformationAction</span></span>
<span data-ttu-id="1dd2f-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1dd2f-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1dd2f-119">하기로</span><span class="sxs-lookup"><span data-stu-id="1dd2f-119">Continue</span></span>
- <span data-ttu-id="1dd2f-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="1dd2f-120">Ignore</span></span>
- <span data-ttu-id="1dd2f-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="1dd2f-121">Inquire</span></span>
- <span data-ttu-id="1dd2f-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1dd2f-122">SilentlyContinue</span></span>
- <span data-ttu-id="1dd2f-123">중지가</span><span class="sxs-lookup"><span data-stu-id="1dd2f-123">Stop</span></span>
- <span data-ttu-id="1dd2f-124">대기</span><span class="sxs-lookup"><span data-stu-id="1dd2f-124">Suspend</span></span>

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

### <span data-ttu-id="1dd2f-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1dd2f-125">-InformationVariable</span></span>
<span data-ttu-id="1dd2f-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1dd2f-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="1dd2f-127">-Profile</span></span>
<span data-ttu-id="1dd2f-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1dd2f-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1dd2f-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1dd2f-130">-ServiceName</span></span>
<span data-ttu-id="1dd2f-131">서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-131">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="1dd2f-132">-슬롯</span><span class="sxs-lookup"><span data-stu-id="1dd2f-132">-Slot</span></span>
<span data-ttu-id="1dd2f-133">배포 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-133">Specifies the environment of the deployment.</span></span>
<span data-ttu-id="1dd2f-134">유효한 값은 스테이징 또는 프로덕션입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-134">Valid values are: Staging or Production.</span></span>
<span data-ttu-id="1dd2f-135">기본값은 실제 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-135">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd2f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd2f-136">CommonParameters</span></span>
<span data-ttu-id="1dd2f-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd2f-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd2f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd2f-139">입력</span><span class="sxs-lookup"><span data-stu-id="1dd2f-139">INPUTS</span></span>

## <span data-ttu-id="1dd2f-140">출력</span><span class="sxs-lookup"><span data-stu-id="1dd2f-140">OUTPUTS</span></span>

## <span data-ttu-id="1dd2f-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1dd2f-141">NOTES</span></span>

## <span data-ttu-id="1dd2f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dd2f-142">RELATED LINKS</span></span>

[<span data-ttu-id="1dd2f-143">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="1dd2f-143">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="1dd2f-144">이동-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="1dd2f-144">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="1dd2f-145">새 AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="1dd2f-145">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="1dd2f-146">-AzureDeployment 제거</span><span class="sxs-lookup"><span data-stu-id="1dd2f-146">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="1dd2f-147">Set AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="1dd2f-147">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


