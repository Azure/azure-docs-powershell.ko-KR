---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 6d1a891dbef40a6556e3a8f2ca122f2c3b46cb28
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880762"
---
# <span data-ttu-id="5c515-101">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5c515-101">New-AzureRmContainerService</span></span>

## <span data-ttu-id="5c515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c515-102">SYNOPSIS</span></span>
<span data-ttu-id="5c515-103">컨테이너 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-103">Creates a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c515-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c515-104">SYNTAX</span></span>

```
New-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c515-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c515-105">DESCRIPTION</span></span>
<span data-ttu-id="5c515-106">**AzureRmContainerService** cmdlet은 컨테이너 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-106">The **New-AzureRmContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="5c515-107">New-AzureRmContainerServiceConfig cmdlet을 사용 하 여 만들 수 있는 컨테이너 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-107">Specify a container service object that you can create by using the New-AzureRmContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="5c515-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5c515-108">EXAMPLES</span></span>

### <span data-ttu-id="5c515-109">예제 1: 컨테이너 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="5c515-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzureRMResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="5c515-110">첫 번째 명령은 지정 된 위치에 ResourceGroup17 이라는 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="5c515-111">자세한 내용은 New-AzureRmResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5c515-111">For more information, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="5c515-112">두 번째 명령은 컨테이너를 만든 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5c515-113">자세한 내용은 New-AzureRmContainerServiceConfig cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5c515-113">For more information, see the New-AzureRmContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="5c515-114">마지막 명령은 $Container에 저장 된 컨테이너에 대 한 컨테이너 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="5c515-115">서비스 이름은 csResourceGroup17입니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="5c515-116">변수</span><span class="sxs-lookup"><span data-stu-id="5c515-116">PARAMETERS</span></span>

### <span data-ttu-id="5c515-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c515-117">-AsJob</span></span>
<span data-ttu-id="5c515-118">RRun에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5c515-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="5c515-119">-ContainerService</span></span>
<span data-ttu-id="5c515-120">새 서비스에 대 한 속성을 포함 하는 컨테이너 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="5c515-121">**ContainerService** 개체를 가져오려면 New-AzureRmContainerServiceConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-121">To obtain a **ContainerService** object, use the New-AzureRmContainerServiceConfig cmdlet.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c515-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c515-122">-DefaultProfile</span></span>
<span data-ttu-id="5c515-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c515-124">-이름</span><span class="sxs-lookup"><span data-stu-id="5c515-124">-Name</span></span>
<span data-ttu-id="5c515-125">이 cmdlet이 만드는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-125">Specifies the name of the container service that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c515-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c515-126">-ResourceGroupName</span></span>
<span data-ttu-id="5c515-127">이 cmdlet이 컨테이너 서비스를 배포 하는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="5c515-128">-확인</span><span class="sxs-lookup"><span data-stu-id="5c515-128">-Confirm</span></span>
<span data-ttu-id="5c515-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c515-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c515-130">-WhatIf</span></span>
<span data-ttu-id="5c515-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5c515-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c515-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c515-133">CommonParameters</span></span>
<span data-ttu-id="5c515-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c515-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c515-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c515-136">입력</span><span class="sxs-lookup"><span data-stu-id="5c515-136">INPUTS</span></span>

### <span data-ttu-id="5c515-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="5c515-137">ContainerService</span></span>
<span data-ttu-id="5c515-138">' ContainerService ' 매개 변수는 파이프라인에서 ' ContainerService ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c515-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="5c515-139">출력</span><span class="sxs-lookup"><span data-stu-id="5c515-139">OUTPUTS</span></span>

### <span data-ttu-id="5c515-140">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="5c515-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="5c515-141">상속자</span><span class="sxs-lookup"><span data-stu-id="5c515-141">NOTES</span></span>

## <span data-ttu-id="5c515-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c515-142">RELATED LINKS</span></span>

[<span data-ttu-id="5c515-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5c515-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="5c515-144">새로운 AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="5c515-144">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="5c515-145">제거-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5c515-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="5c515-146">업데이트-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5c515-146">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)

