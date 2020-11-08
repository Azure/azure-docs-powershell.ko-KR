---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 9709a21f51b1f0d2b9701257b8c5556698cab228
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041603"
---
# <span data-ttu-id="7c55b-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7c55b-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="7c55b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c55b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c55b-103">배포 가져오기 작업</span><span class="sxs-lookup"><span data-stu-id="7c55b-103">Get deployment operation</span></span>

## <span data-ttu-id="7c55b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c55b-104">SYNTAX</span></span>

### <span data-ttu-id="7c55b-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c55b-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c55b-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="7c55b-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c55b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7c55b-107">DESCRIPTION</span></span>
<span data-ttu-id="7c55b-108">**AzDeploymentOperation** cmdlet에는 특정 배포에 대해 실패 한 정확한 작업에 대 한 자세한 정보를 식별 하 고 제공 하는 데 도움이 되는 배포의 일부인 모든 작업이 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="7c55b-109">또한 각 배포 작업에 대 한 응답 및 요청 콘텐츠를 표시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="7c55b-110">포털의 배포 세부 정보에 제공 되는 정보와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="7c55b-111">요청 및 응답 콘텐츠를 가져오려면 **새 AzDeployment** 를 통해 배포를 제출할 때이 설정을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="7c55b-112">배포 작업을 검색할 때 반환 되는 리소스 속성 또는 **Listkeys** 작업에 사용 되는 암호와 같은 비밀을 기록 하 고 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="7c55b-113">이 설정 및이 설정을 사용 하는 방법에 대 한 자세한 내용은 ARM 서식 파일 배포 New-AzDeployment 및 디버깅을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c55b-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="7c55b-114">예제의</span><span class="sxs-lookup"><span data-stu-id="7c55b-114">EXAMPLES</span></span>

### <span data-ttu-id="7c55b-115">배포 이름이 지정 된 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c55b-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="7c55b-116">현재 구독 범위에서 이름이 "test" 인 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="7c55b-117">배포 가져오기 및 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="7c55b-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="7c55b-118">이 명령은 현재 구독 범위에서 "test" 배포를 가져와 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="7c55b-119">변수</span><span class="sxs-lookup"><span data-stu-id="7c55b-119">PARAMETERS</span></span>

### <span data-ttu-id="7c55b-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7c55b-120">-ApiVersion</span></span>
<span data-ttu-id="7c55b-121">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7c55b-122">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-122">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c55b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c55b-123">-DefaultProfile</span></span>
<span data-ttu-id="7c55b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c55b-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="7c55b-125">-DeploymentName</span></span>
<span data-ttu-id="7c55b-126">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-126">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c55b-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="7c55b-127">-DeploymentObject</span></span>
<span data-ttu-id="7c55b-128">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-128">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c55b-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7c55b-129">-OperationId</span></span>
<span data-ttu-id="7c55b-130">배포 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-130">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c55b-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="7c55b-131">-Pre</span></span>
<span data-ttu-id="7c55b-132">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c55b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c55b-133">CommonParameters</span></span>
<span data-ttu-id="7c55b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c55b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c55b-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c55b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c55b-136">입력</span><span class="sxs-lookup"><span data-stu-id="7c55b-136">INPUTS</span></span>

### <span data-ttu-id="7c55b-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7c55b-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="7c55b-138">출력</span><span class="sxs-lookup"><span data-stu-id="7c55b-138">OUTPUTS</span></span>

### <span data-ttu-id="7c55b-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7c55b-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="7c55b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="7c55b-140">NOTES</span></span>

## <span data-ttu-id="7c55b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c55b-141">RELATED LINKS</span></span>
