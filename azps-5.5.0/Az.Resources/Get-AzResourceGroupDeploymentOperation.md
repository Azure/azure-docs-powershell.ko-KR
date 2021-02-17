---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 1ac0ab153177caaf080e5aa9144020ea253b8438
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206016"
---
# <span data-ttu-id="41441-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="41441-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="41441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41441-102">SYNOPSIS</span></span>
<span data-ttu-id="41441-103">리소스 그룹 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="41441-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="41441-104">구문</span><span class="sxs-lookup"><span data-stu-id="41441-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41441-105">설명</span><span class="sxs-lookup"><span data-stu-id="41441-105">DESCRIPTION</span></span>
<span data-ttu-id="41441-106">**Get-AzResourceGroupDeploymentOperation** cmdlet에는 특정 배포에 실패한 정확한 작업에 대한 자세한 정보를 식별하고 제공하기 위해 배포의 일부인 모든 작업이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="41441-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="41441-107">또한 각 배포 작업에 대한 응답 및 요청 콘텐츠를 보여 주어도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="41441-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="41441-108">이는 포털의 배포 세부 정보에 제공된 동일한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="41441-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="41441-109">요청 및 응답 콘텐츠를 얻습니다. **New-AzResourceGroupDeployment를** 통해 배포를 제출할 때 설정을 사용하도록 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="41441-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="41441-110">잠재적으로 배포 작업을 검색할 때 반환되는 리소스 속성 또는 **listKeys** 작업에 사용되는 암호와 같은 비밀을 기록하고 노출할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41441-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="41441-111">이 설정 및 사용하도록 설정하는 방법에 대한 자세한 내용은 템플릿 배포에 대한 New-AzResourceGroupDeployment 및 디버깅을 ARM 참조</span><span class="sxs-lookup"><span data-stu-id="41441-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="41441-112">예제</span><span class="sxs-lookup"><span data-stu-id="41441-112">EXAMPLES</span></span>

### <span data-ttu-id="41441-113">예제 1: Get1</span><span class="sxs-lookup"><span data-stu-id="41441-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="41441-114">리소스 그룹 "test"에서 이름이 "test"인 배포 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="41441-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="41441-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41441-115">PARAMETERS</span></span>

### <span data-ttu-id="41441-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41441-116">-DefaultProfile</span></span>
<span data-ttu-id="41441-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41441-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41441-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="41441-118">-DeploymentName</span></span>
<span data-ttu-id="41441-119">배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41441-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41441-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="41441-120">-Pre</span></span>
<span data-ttu-id="41441-121">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="41441-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="41441-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41441-122">-ResourceGroupName</span></span>
<span data-ttu-id="41441-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="41441-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41441-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41441-124">-SubscriptionId</span></span>
<span data-ttu-id="41441-125">사용할 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41441-125">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41441-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41441-126">CommonParameters</span></span>
<span data-ttu-id="41441-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="41441-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41441-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41441-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41441-129">입력</span><span class="sxs-lookup"><span data-stu-id="41441-129">INPUTS</span></span>

### <span data-ttu-id="41441-130">System.String</span><span class="sxs-lookup"><span data-stu-id="41441-130">System.String</span></span>

### <span data-ttu-id="41441-131">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="41441-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="41441-132">출력</span><span class="sxs-lookup"><span data-stu-id="41441-132">OUTPUTS</span></span>

### <span data-ttu-id="41441-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="41441-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="41441-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="41441-134">NOTES</span></span>

## <span data-ttu-id="41441-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41441-135">RELATED LINKS</span></span>
