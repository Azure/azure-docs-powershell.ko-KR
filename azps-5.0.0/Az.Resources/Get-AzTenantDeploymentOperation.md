---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308813"
---
# <span data-ttu-id="8b330-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8b330-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="8b330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b330-102">SYNOPSIS</span></span>
<span data-ttu-id="8b330-103">테 넌 트 범위에서 배포에 대 한 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="8b330-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="8b330-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8b330-104">SYNTAX</span></span>

### <span data-ttu-id="8b330-105">GetByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8b330-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b330-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="8b330-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b330-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8b330-107">DESCRIPTION</span></span>
<span data-ttu-id="8b330-108">**AzTenantDeploymentOperation** cmdlet은 특정 배포에 대해 실패 한 정확한 작업에 대 한 자세한 정보를 식별 하 고 제공 하는 데 도움이 되도록 현재 테 넌 트 범위에서 배포의 일부인 모든 작업을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b330-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="8b330-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8b330-109">EXAMPLES</span></span>

### <span data-ttu-id="8b330-110">예제 1: 배포 이름이 지정 된 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="8b330-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="8b330-111">현재 테 넌 트 범위에서 이름이 "Deploy01" 인 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b330-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="8b330-112">예제 2: 배포 가져오기 및 배포 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="8b330-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="8b330-113">이 명령은 현재 테 넌 트 범위에서 배포 "Deploy01"를 가져와 배포 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b330-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="8b330-114">변수</span><span class="sxs-lookup"><span data-stu-id="8b330-114">PARAMETERS</span></span>

### <span data-ttu-id="8b330-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b330-115">-DefaultProfile</span></span>
<span data-ttu-id="8b330-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b330-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b330-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="8b330-117">-DeploymentName</span></span>
<span data-ttu-id="8b330-118">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b330-118">The deployment name.</span></span>

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

### <span data-ttu-id="8b330-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="8b330-119">-DeploymentObject</span></span>
<span data-ttu-id="8b330-120">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8b330-120">The deployment object.</span></span>

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

### <span data-ttu-id="8b330-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="8b330-121">-OperationId</span></span>
<span data-ttu-id="8b330-122">배포 작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8b330-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="8b330-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="8b330-123">-Pre</span></span>
<span data-ttu-id="8b330-124">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8b330-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8b330-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b330-125">CommonParameters</span></span>
<span data-ttu-id="8b330-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b330-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b330-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8b330-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b330-128">입력</span><span class="sxs-lookup"><span data-stu-id="8b330-128">INPUTS</span></span>

### <span data-ttu-id="8b330-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="8b330-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8b330-130">출력</span><span class="sxs-lookup"><span data-stu-id="8b330-130">OUTPUTS</span></span>

### <span data-ttu-id="8b330-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8b330-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="8b330-132">상속자</span><span class="sxs-lookup"><span data-stu-id="8b330-132">NOTES</span></span>

## <span data-ttu-id="8b330-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b330-133">RELATED LINKS</span></span>
