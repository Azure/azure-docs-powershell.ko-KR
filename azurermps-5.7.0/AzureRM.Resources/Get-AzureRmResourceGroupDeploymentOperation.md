---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
ms.openlocfilehash: 557aa312200a2e5c49e33f8a176079ee4b27b629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528841"
---
# <span data-ttu-id="261b5-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="261b5-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="261b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="261b5-102">SYNOPSIS</span></span>
<span data-ttu-id="261b5-103">리소스 그룹 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="261b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="261b5-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="261b5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="261b5-105">DESCRIPTION</span></span>
<span data-ttu-id="261b5-106">**AzureRmResourceGroupDeploymentOperation** cmdlet에는 특정 배포에 대해 실패 한 정확한 작업에 대 한 자세한 정보를 식별 하 고 제공 하는 데 도움이 되는 배포의 일부인 모든 작업이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="261b5-107">또한 각 배포 작업에 대 한 응답 및 요청 콘텐츠를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="261b5-108">포털의 배포 세부 정보에 제공 되는 정보와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-108">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="261b5-109">요청 및 응답 콘텐츠를 가져오려면 **새 AzureRmResourceGroupDeployment** 를 통해 배포를 제출할 때이 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="261b5-110">배포 작업을 검색할 때 반환 되는 리소스 속성 또는 **Listkeys** 작업에 사용 되는 암호와 같은 비밀을 기록 하 고 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="261b5-111">이 설정 및이 설정을 사용 하는 방법에 대 한 자세한 내용은 ARM 서식 파일 배포 New-AzureRmResourceGroupDeployment 및 디버깅을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="261b5-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="261b5-112">예제의</span><span class="sxs-lookup"><span data-stu-id="261b5-112">EXAMPLES</span></span>

### <span data-ttu-id="261b5-113">Get1</span><span class="sxs-lookup"><span data-stu-id="261b5-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="261b5-114">리소스 그룹 "테스트"에서 이름이 "test" 인 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="261b5-115">변수</span><span class="sxs-lookup"><span data-stu-id="261b5-115">PARAMETERS</span></span>

### <span data-ttu-id="261b5-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="261b5-116">-ApiVersion</span></span>
<span data-ttu-id="261b5-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="261b5-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="261b5-119">-DefaultProfile</span></span>
<span data-ttu-id="261b5-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="261b5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261b5-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="261b5-121">-DeploymentName</span></span>
<span data-ttu-id="261b5-122">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261b5-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="261b5-123">-InformationAction</span></span>
<span data-ttu-id="261b5-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="261b5-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="261b5-126">하기로</span><span class="sxs-lookup"><span data-stu-id="261b5-126">Continue</span></span>
- <span data-ttu-id="261b5-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="261b5-127">Ignore</span></span>
- <span data-ttu-id="261b5-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="261b5-128">Inquire</span></span>
- <span data-ttu-id="261b5-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="261b5-129">SilentlyContinue</span></span>
- <span data-ttu-id="261b5-130">중지가</span><span class="sxs-lookup"><span data-stu-id="261b5-130">Stop</span></span>
- <span data-ttu-id="261b5-131">대기</span><span class="sxs-lookup"><span data-stu-id="261b5-131">Suspend</span></span>

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

### <span data-ttu-id="261b5-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="261b5-132">-InformationVariable</span></span>
<span data-ttu-id="261b5-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="261b5-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="261b5-134">-Pre</span></span>
<span data-ttu-id="261b5-135">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="261b5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="261b5-136">-ResourceGroupName</span></span>
<span data-ttu-id="261b5-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="261b5-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="261b5-138">-SubscriptionId</span></span>
<span data-ttu-id="261b5-139">사용할 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-139">The subscription to use.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="261b5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="261b5-140">CommonParameters</span></span>
<span data-ttu-id="261b5-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="261b5-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="261b5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="261b5-143">입력</span><span class="sxs-lookup"><span data-stu-id="261b5-143">INPUTS</span></span>

### <span data-ttu-id="261b5-144">Shap</span><span class="sxs-lookup"><span data-stu-id="261b5-144">Guid</span></span>
<span data-ttu-id="261b5-145">' SubscriptionId ' 매개 변수는 파이프라인에서 ' Guid ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="261b5-145">Parameter 'SubscriptionId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="261b5-146">출력</span><span class="sxs-lookup"><span data-stu-id="261b5-146">OUTPUTS</span></span>

### <span data-ttu-id="261b5-147">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="261b5-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="261b5-148">상속자</span><span class="sxs-lookup"><span data-stu-id="261b5-148">NOTES</span></span>

## <span data-ttu-id="261b5-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="261b5-149">RELATED LINKS</span></span>
