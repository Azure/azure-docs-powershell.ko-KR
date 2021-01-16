---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325366"
---
# <span data-ttu-id="a1ed8-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a1ed8-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="a1ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ed8-103">배포 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="a1ed8-103">Get deployment operation</span></span>

## <span data-ttu-id="a1ed8-104">구문</span><span class="sxs-lookup"><span data-stu-id="a1ed8-104">SYNTAX</span></span>

### <span data-ttu-id="a1ed8-105">GetByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a1ed8-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1ed8-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a1ed8-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1ed8-107">설명</span><span class="sxs-lookup"><span data-stu-id="a1ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="a1ed8-108">**Get-AzDeploymentOperation** cmdlet은 특정 배포에 실패한 정확한 작업에 대한 자세한 정보를 식별하고 제공하기 위해 배포의 일부인 모든 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="a1ed8-109">또한 각 배포 작업에 대한 응답 및 요청 콘텐츠를 보여 주어도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="a1ed8-110">이는 포털의 배포 세부 정보에 제공된 동일한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="a1ed8-111">요청 및 응답 콘텐츠를 얻습니다. **New-AzDeployment를** 통해 배포를 제출할 때 설정을 사용하도록 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="a1ed8-112">잠재적으로 배포 작업을 검색할 때 반환되는 리소스 속성 또는 **listKeys** 작업에 사용되는 암호와 같은 비밀을 기록하고 노출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="a1ed8-113">이 설정 및 사용하도록 설정하는 방법에 대한 자세한 내용은 템플릿 배포에 대한 New-AzDeployment 및 디버깅을 ARM 참조</span><span class="sxs-lookup"><span data-stu-id="a1ed8-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="a1ed8-114">예제</span><span class="sxs-lookup"><span data-stu-id="a1ed8-114">EXAMPLES</span></span>

### <span data-ttu-id="a1ed8-115">예제 1: 배포 이름을 지정한 배포 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="a1ed8-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="a1ed8-116">현재 구독 범위에서 이름이 "test"인 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="a1ed8-117">예제 2: 배포를 시작하고 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="a1ed8-118">이 명령은 현재 구독 범위에서 배포 "테스트"를 수행하고 해당 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="a1ed8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1ed8-119">PARAMETERS</span></span>

### <span data-ttu-id="a1ed8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ed8-120">-DefaultProfile</span></span>
<span data-ttu-id="a1ed8-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1ed8-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a1ed8-122">-DeploymentName</span></span>
<span data-ttu-id="a1ed8-123">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-123">The deployment name.</span></span>

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

### <span data-ttu-id="a1ed8-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a1ed8-124">-DeploymentObject</span></span>
<span data-ttu-id="a1ed8-125">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-125">The deployment object.</span></span>

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

### <span data-ttu-id="a1ed8-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a1ed8-126">-OperationId</span></span>
<span data-ttu-id="a1ed8-127">배포 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="a1ed8-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="a1ed8-128">-Pre</span></span>
<span data-ttu-id="a1ed8-129">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a1ed8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ed8-130">CommonParameters</span></span>
<span data-ttu-id="a1ed8-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ed8-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a1ed8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ed8-133">입력</span><span class="sxs-lookup"><span data-stu-id="a1ed8-133">INPUTS</span></span>

### <span data-ttu-id="a1ed8-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="a1ed8-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a1ed8-135">출력</span><span class="sxs-lookup"><span data-stu-id="a1ed8-135">OUTPUTS</span></span>

### <span data-ttu-id="a1ed8-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a1ed8-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="a1ed8-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a1ed8-137">NOTES</span></span>

## <span data-ttu-id="a1ed8-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1ed8-138">RELATED LINKS</span></span>
