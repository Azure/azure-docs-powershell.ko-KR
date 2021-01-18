---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: 58ae996e4d2723d4b38b548dd8225a2a483ce8f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496043"
---
# <span data-ttu-id="b6949-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="b6949-101">New-AzHost</span></span>

## <span data-ttu-id="b6949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6949-102">SYNOPSIS</span></span>
<span data-ttu-id="b6949-103">호스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-103">Creates a  host.</span></span>

## <span data-ttu-id="b6949-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6949-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6949-105">설명</span><span class="sxs-lookup"><span data-stu-id="b6949-105">DESCRIPTION</span></span>
<span data-ttu-id="b6949-106">이 cmdlet은 호스트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="b6949-107">예제</span><span class="sxs-lookup"><span data-stu-id="b6949-107">EXAMPLES</span></span>

### <span data-ttu-id="b6949-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6949-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="b6949-109">이 명령은 주어진 호스트 그룹 및 주어진 위치에 주어진 SKU의 호스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="b6949-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6949-110">PARAMETERS</span></span>

### <span data-ttu-id="b6949-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6949-111">-AsJob</span></span>
<span data-ttu-id="b6949-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b6949-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6949-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="b6949-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="b6949-114">오류가 발생하면 호스트를 자동으로 대체할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="b6949-115">값이 제공되지 않을 때 기본값은 'true'입니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-115">The value is defaulted to 'true' when not provided.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6949-116">-DefaultProfile</span></span>
<span data-ttu-id="b6949-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6949-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="b6949-118">-HostGroupName</span></span>
<span data-ttu-id="b6949-119">호스트 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-119">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b6949-120">-LicenseType</span></span>
<span data-ttu-id="b6949-121">호스트에 배포된 VM에 적용할 소프트웨어 라이선스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="b6949-122">가능한 값은 None, Windows_Server_Hybrid 및 Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="b6949-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="b6949-123">기본값은 None입니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-124">-Location</span><span class="sxs-lookup"><span data-stu-id="b6949-124">-Location</span></span>
<span data-ttu-id="b6949-125">위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b6949-126">-Name</span></span>
<span data-ttu-id="b6949-127">호스트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="b6949-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="b6949-129">호스트의 플랫폼 장애 도메인 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="b6949-130">그런 다음, 최소값은 0, 최대값은 2입니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-130">Then minimum value is 0 and the maximum value is 2.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6949-131">-ResourceGroupName</span></span>
<span data-ttu-id="b6949-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="b6949-133">-Sku</span></span>
<span data-ttu-id="b6949-134">SKU의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-134">Specifies the name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="b6949-135">-Tag</span></span>
<span data-ttu-id="b6949-136">태그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-136">Specifies Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6949-137">-Confirm</span></span>
<span data-ttu-id="b6949-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6949-139">-WhatIf</span></span>
<span data-ttu-id="b6949-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b6949-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6949-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6949-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6949-142">CommonParameters</span></span>
<span data-ttu-id="b6949-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6949-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6949-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6949-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6949-145">입력</span><span class="sxs-lookup"><span data-stu-id="b6949-145">INPUTS</span></span>

### <span data-ttu-id="b6949-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b6949-146">System.String</span></span>

## <span data-ttu-id="b6949-147">출력</span><span class="sxs-lookup"><span data-stu-id="b6949-147">OUTPUTS</span></span>

### <span data-ttu-id="b6949-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="b6949-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="b6949-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6949-149">NOTES</span></span>

## <span data-ttu-id="b6949-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6949-150">RELATED LINKS</span></span>
