---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 23d14e88d7778402d69a6ea3248fa499e5e829cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496101"
---
# <span data-ttu-id="d5e7c-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d5e7c-101">Get-AzContainerService</span></span>

## <span data-ttu-id="d5e7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e7c-103">컨테이너 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-103">Gets a container service.</span></span>

## <span data-ttu-id="d5e7c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d5e7c-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5e7c-105">설명</span><span class="sxs-lookup"><span data-stu-id="d5e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="d5e7c-106">**Get-AzContainerService** cmdlet은 컨테이너 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="d5e7c-107">상태, 마스터 및 에이전트 수 및 마스터 및 에이전트의 정식 도메인 이름을 포함 하는 컨테이너 서비스의 속성을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="d5e7c-108">예제</span><span class="sxs-lookup"><span data-stu-id="d5e7c-108">EXAMPLES</span></span>

### <span data-ttu-id="d5e7c-109">예제 1: 컨테이너 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="d5e7c-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"

ResourceGroupName     : ResourceGroup17
ProvisioningState     : Succeeded
OrchestratorProfile   :
  OrchestratorType    : DCOS
MasterProfile         :
  Count               : 1
  DnsPrefix           : MasterResourceGroup17
  Fqdn                : masterresourcegroup17.eastus.cloudapp.azure.com
AgentPoolProfiles[0]  :
  Name                : AgentPool01
  Count               : 2
  VmSize              : Standard_A1
  DnsPrefix           : APResourceGroup17
  Fqdn                : apresourcegroup17.eastus.cloudapp.azure.com
LinuxProfile          :
  AdminUsername       : acslinuxadmin
  Ssh                 :
    PublicKeys[0]     :
      KeyData         : ssh-rsa xxxxxxxxxxxxxx contoso@microsoft.com
DiagnosticsProfile    :
  VmDiagnostics       :
    Enabled           : False
    StorageUri        : https://xxxxxxxxxxx.blob.core.windows.net/
Id                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup17/providers/Micr
osoft.ContainerService/containerServices/CSResourceGroup17
Name                  : CSResourceGroup17
Type                  : Microsoft.ContainerService/ContainerServices
Location              : eastus
Tags                  : {}
```

<span data-ttu-id="d5e7c-110">이 명령은 CSResourceGroup17이라는 컨테이너 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="d5e7c-111">예제 2: 모든 컨테이너 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="d5e7c-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="d5e7c-112">이 명령은 구독의 모든 컨테이너 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="d5e7c-113">예제 3: 리소스 그룹의 모든 컨테이너 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="d5e7c-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="d5e7c-114">이 명령은 ResourceGroup17의 모든 컨테이너 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="d5e7c-115">예제 4: 필터를 사용하여 모든 컨테이너 서비스 얻기</span><span class="sxs-lookup"><span data-stu-id="d5e7c-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="d5e7c-116">이 명령은 "CSResourceGroup1"으로 시작하는 모든 컨테이너 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="d5e7c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5e7c-117">PARAMETERS</span></span>

### <span data-ttu-id="d5e7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e7c-118">-DefaultProfile</span></span>
<span data-ttu-id="d5e7c-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5e7c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d5e7c-120">-Name</span></span>
<span data-ttu-id="d5e7c-121">이 cmdlet이 제공하는 컨테이너 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-121">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d5e7c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e7c-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5e7c-123">이 cmdlet이 제공하는 컨테이너 서비스의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d5e7c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e7c-124">CommonParameters</span></span>
<span data-ttu-id="d5e7c-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e7c-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5e7c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e7c-127">입력</span><span class="sxs-lookup"><span data-stu-id="d5e7c-127">INPUTS</span></span>

### <span data-ttu-id="d5e7c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d5e7c-128">System.String</span></span>

## <span data-ttu-id="d5e7c-129">출력</span><span class="sxs-lookup"><span data-stu-id="d5e7c-129">OUTPUTS</span></span>

### <span data-ttu-id="d5e7c-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d5e7c-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d5e7c-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d5e7c-131">NOTES</span></span>

## <span data-ttu-id="d5e7c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5e7c-132">RELATED LINKS</span></span>

[<span data-ttu-id="d5e7c-133">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d5e7c-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="d5e7c-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d5e7c-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="d5e7c-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d5e7c-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


