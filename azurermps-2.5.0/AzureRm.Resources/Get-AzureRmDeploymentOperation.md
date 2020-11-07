---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeploymentoperation
schema: 2.0.0
ms.openlocfilehash: 2bb5c3823d974dad53045d9283099befd4d60855
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882802"
---
# <span data-ttu-id="d496f-101">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d496f-101">Get-AzureRmDeploymentOperation</span></span>

## <span data-ttu-id="d496f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d496f-102">SYNOPSIS</span></span>
<span data-ttu-id="d496f-103">배포 가져오기 작업</span><span class="sxs-lookup"><span data-stu-id="d496f-103">Get deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d496f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d496f-104">SYNTAX</span></span>

### <span data-ttu-id="d496f-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d496f-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d496f-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d496f-106">GetByDeploymentObject</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d496f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d496f-107">DESCRIPTION</span></span>
<span data-ttu-id="d496f-108">**AzureRmDeploymentOperation** cmdlet에는 특정 배포에 대해 실패 한 정확한 작업에 대 한 자세한 정보를 식별 하 고 제공 하는 데 도움이 되는 배포의 일부인 모든 작업이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-108">The **Get-AzureRmDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="d496f-109">또한 각 배포 작업에 대 한 응답 및 요청 콘텐츠를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="d496f-110">포털의 배포 세부 정보에 제공 되는 정보와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="d496f-111">요청 및 응답 콘텐츠를 가져오려면 **새 AzureRmDeployment** 를 통해 배포를 제출할 때이 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmDeployment**.</span></span>
<span data-ttu-id="d496f-112">배포 작업을 검색할 때 반환 되는 리소스 속성 또는 **Listkeys** 작업에 사용 되는 암호와 같은 비밀을 기록 하 고 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="d496f-113">이 설정 및이 설정을 사용 하는 방법에 대 한 자세한 내용은 ARM 서식 파일 배포 New-AzureRmDeployment 및 디버깅을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d496f-113">For more on this setting and how to enable it, see New-AzureRmDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="d496f-114">예제의</span><span class="sxs-lookup"><span data-stu-id="d496f-114">EXAMPLES</span></span>

### <span data-ttu-id="d496f-115">배포 이름이 지정 된 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="d496f-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzureRmDeploymentOperation -DeploymentName test
```

<span data-ttu-id="d496f-116">현재 구독 범위에서 이름이 "test" 인 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="d496f-117">배포 가져오기 및 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="d496f-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "test" | Get-AzureRmDeploymentOperation
```

<span data-ttu-id="d496f-118">이 명령은 현재 구독 범위에서 "test" 배포를 가져와 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="d496f-119">변수</span><span class="sxs-lookup"><span data-stu-id="d496f-119">PARAMETERS</span></span>

### <span data-ttu-id="d496f-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d496f-120">-ApiVersion</span></span>
<span data-ttu-id="d496f-121">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d496f-122">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d496f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d496f-123">-DefaultProfile</span></span>
<span data-ttu-id="d496f-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d496f-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d496f-125">-DeploymentName</span></span>
<span data-ttu-id="d496f-126">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-126">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d496f-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d496f-127">-DeploymentObject</span></span>
<span data-ttu-id="d496f-128">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-128">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d496f-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d496f-129">-OperationId</span></span>
<span data-ttu-id="d496f-130">배포 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-130">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d496f-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="d496f-131">-Pre</span></span>
<span data-ttu-id="d496f-132">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d496f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d496f-133">CommonParameters</span></span>
<span data-ttu-id="d496f-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d496f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d496f-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d496f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d496f-136">입력</span><span class="sxs-lookup"><span data-stu-id="d496f-136">INPUTS</span></span>

### <span data-ttu-id="d496f-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d496f-137">System.String</span></span>
<span data-ttu-id="d496f-138">시스템 Null 허용 ' 1 [[b77a5c561934e089], mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="d496f-138">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d496f-139">출력</span><span class="sxs-lookup"><span data-stu-id="d496f-139">OUTPUTS</span></span>

### <span data-ttu-id="d496f-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d496f-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="d496f-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d496f-141">NOTES</span></span>

## <span data-ttu-id="d496f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d496f-142">RELATED LINKS</span></span>
