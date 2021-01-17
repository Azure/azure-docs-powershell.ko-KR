---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490460"
---
# <span data-ttu-id="b3fd1-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="b3fd1-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="b3fd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="b3fd1-103">테넌트 범위에서 배포에 대한 배포 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="b3fd1-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="b3fd1-104">구문</span><span class="sxs-lookup"><span data-stu-id="b3fd1-104">SYNTAX</span></span>

### <span data-ttu-id="b3fd1-105">GetByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b3fd1-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3fd1-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="b3fd1-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3fd1-107">설명</span><span class="sxs-lookup"><span data-stu-id="b3fd1-107">DESCRIPTION</span></span>
<span data-ttu-id="b3fd1-108">**Get-AzTenantDeploymentOperation** cmdlet은 특정 배포에 실패한 정확한 작업에 대한 자세한 정보를 식별하고 제공하기 위해 현재 테넌트 범위에서 배포의 일부인 모든 작업을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="b3fd1-109">예제</span><span class="sxs-lookup"><span data-stu-id="b3fd1-109">EXAMPLES</span></span>

### <span data-ttu-id="b3fd1-110">예제 1: 배포 이름을 지정한 배포 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="b3fd1-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="b3fd1-111">현재 테넌트 범위에서 이름이 "Deploy01"인 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="b3fd1-112">예제 2: 배포를 시작하고 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="b3fd1-113">이 명령은 현재 테넌트 범위에서 배포 "Deploy01"을 사용하여 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="b3fd1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3fd1-114">PARAMETERS</span></span>

### <span data-ttu-id="b3fd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3fd1-115">-DefaultProfile</span></span>
<span data-ttu-id="b3fd1-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3fd1-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b3fd1-117">-DeploymentName</span></span>
<span data-ttu-id="b3fd1-118">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-118">The deployment name.</span></span>

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

### <span data-ttu-id="b3fd1-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="b3fd1-119">-DeploymentObject</span></span>
<span data-ttu-id="b3fd1-120">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-120">The deployment object.</span></span>

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

### <span data-ttu-id="b3fd1-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b3fd1-121">-OperationId</span></span>
<span data-ttu-id="b3fd1-122">배포 작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="b3fd1-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="b3fd1-123">-Pre</span></span>
<span data-ttu-id="b3fd1-124">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b3fd1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3fd1-125">CommonParameters</span></span>
<span data-ttu-id="b3fd1-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3fd1-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3fd1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3fd1-128">입력</span><span class="sxs-lookup"><span data-stu-id="b3fd1-128">INPUTS</span></span>

### <span data-ttu-id="b3fd1-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="b3fd1-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b3fd1-130">출력</span><span class="sxs-lookup"><span data-stu-id="b3fd1-130">OUTPUTS</span></span>

### <span data-ttu-id="b3fd1-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="b3fd1-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="b3fd1-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b3fd1-132">NOTES</span></span>

## <span data-ttu-id="b3fd1-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3fd1-133">RELATED LINKS</span></span>
