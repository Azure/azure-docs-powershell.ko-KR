---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: b8f453200f2365272461373214ec92580212c4b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877019"
---
# <span data-ttu-id="18759-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="18759-101">New-AzContainerService</span></span>

## <span data-ttu-id="18759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18759-102">SYNOPSIS</span></span>
<span data-ttu-id="18759-103">컨테이너 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18759-103">Creates a container service.</span></span>

## <span data-ttu-id="18759-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18759-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18759-105">설명은</span><span class="sxs-lookup"><span data-stu-id="18759-105">DESCRIPTION</span></span>
<span data-ttu-id="18759-106">**AzContainerService** cmdlet은 컨테이너 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18759-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="18759-107">New-AzContainerServiceConfig cmdlet을 사용 하 여 만들 수 있는 컨테이너 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18759-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="18759-108">예제의</span><span class="sxs-lookup"><span data-stu-id="18759-108">EXAMPLES</span></span>

### <span data-ttu-id="18759-109">예제 1: 컨테이너 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="18759-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="18759-110">첫 번째 명령은 지정 된 위치에 ResourceGroup17 이라는 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18759-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="18759-111">자세한 내용은 New-AzResourceGroup cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18759-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="18759-112">두 번째 명령은 컨테이너를 만든 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="18759-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="18759-113">자세한 내용은 New-AzContainerServiceConfig cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="18759-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>

<span data-ttu-id="18759-114">마지막 명령은 $Container에 저장 된 컨테이너에 대 한 컨테이너 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="18759-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="18759-115">서비스 이름은 csResourceGroup17입니다.</span><span class="sxs-lookup"><span data-stu-id="18759-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="18759-116">변수</span><span class="sxs-lookup"><span data-stu-id="18759-116">PARAMETERS</span></span>

### <span data-ttu-id="18759-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18759-117">-AsJob</span></span>
<span data-ttu-id="18759-118">RRun에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="18759-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="18759-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="18759-119">-ContainerService</span></span>
<span data-ttu-id="18759-120">새 서비스에 대 한 속성을 포함 하는 컨테이너 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18759-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="18759-121">**ContainerService** 개체를 가져오려면 New-AzContainerServiceConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="18759-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="18759-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18759-122">-DefaultProfile</span></span>
<span data-ttu-id="18759-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="18759-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18759-124">-이름</span><span class="sxs-lookup"><span data-stu-id="18759-124">-Name</span></span>
<span data-ttu-id="18759-125">이 cmdlet이 만드는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18759-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="18759-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18759-126">-ResourceGroupName</span></span>
<span data-ttu-id="18759-127">이 cmdlet이 컨테이너 서비스를 배포 하는 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18759-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="18759-128">-확인</span><span class="sxs-lookup"><span data-stu-id="18759-128">-Confirm</span></span>
<span data-ttu-id="18759-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="18759-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18759-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18759-130">-WhatIf</span></span>
<span data-ttu-id="18759-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="18759-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="18759-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18759-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18759-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18759-133">CommonParameters</span></span>
<span data-ttu-id="18759-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18759-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18759-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18759-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18759-136">입력</span><span class="sxs-lookup"><span data-stu-id="18759-136">INPUTS</span></span>

### <span data-ttu-id="18759-137">ContainerService</span><span class="sxs-lookup"><span data-stu-id="18759-137">ContainerService</span></span>
<span data-ttu-id="18759-138">' ContainerService ' 매개 변수는 파이프라인에서 ' ContainerService ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="18759-138">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="18759-139">출력</span><span class="sxs-lookup"><span data-stu-id="18759-139">OUTPUTS</span></span>

### <span data-ttu-id="18759-140">PSContainerService의. m a.</span><span class="sxs-lookup"><span data-stu-id="18759-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="18759-141">상속자</span><span class="sxs-lookup"><span data-stu-id="18759-141">NOTES</span></span>

## <span data-ttu-id="18759-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18759-142">RELATED LINKS</span></span>

[<span data-ttu-id="18759-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="18759-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="18759-144">새로운 AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="18759-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="18759-145">제거-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="18759-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="18759-146">업데이트-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="18759-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


