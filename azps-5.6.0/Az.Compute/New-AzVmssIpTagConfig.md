---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: 241b8938be77d9074000a116f82d8b2bcdffc5b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007072"
---
# <span data-ttu-id="6dfac-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="6dfac-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="6dfac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dfac-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfac-103">VMSS의 네트워크 인터페이스에 대한 IP 태그 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="6dfac-104">구문</span><span class="sxs-lookup"><span data-stu-id="6dfac-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dfac-105">설명</span><span class="sxs-lookup"><span data-stu-id="6dfac-105">DESCRIPTION</span></span>
<span data-ttu-id="6dfac-106">**New-AzVmssIpTagConfig** cmdlet은 VMSS(Virtual Machine Scale Set)의 네트워크 인터페이스에 대한 IP 태그 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="6dfac-107">이 cmdlet에서 구성을 cmdlet의 *IPTag* 매개 변수로 New-AzVmssIpConfig 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="6dfac-108">예제</span><span class="sxs-lookup"><span data-stu-id="6dfac-108">EXAMPLES</span></span>

### <span data-ttu-id="6dfac-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="6dfac-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="6dfac-110">이 명령은 'FirstPartyUsage' 형식 및 'Sql' 태그가 있는 IP 태그 로컬 개체를 만든 다음 이 IP 태그를 사용하여 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="6dfac-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6dfac-111">PARAMETERS</span></span>

### <span data-ttu-id="6dfac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfac-112">-DefaultProfile</span></span>
<span data-ttu-id="6dfac-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dfac-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="6dfac-114">-IpTagType</span></span>
<span data-ttu-id="6dfac-115">IP 태그 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="6dfac-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="6dfac-116">-Tag</span></span>
<span data-ttu-id="6dfac-117">IP 태그 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-117">Specifies an IP Tag Value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dfac-118">-확인</span><span class="sxs-lookup"><span data-stu-id="6dfac-118">-Confirm</span></span>
<span data-ttu-id="6dfac-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dfac-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dfac-120">-WhatIf</span></span>
<span data-ttu-id="6dfac-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dfac-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dfac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfac-123">CommonParameters</span></span>
<span data-ttu-id="6dfac-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6dfac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfac-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dfac-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfac-126">입력</span><span class="sxs-lookup"><span data-stu-id="6dfac-126">INPUTS</span></span>

### <span data-ttu-id="6dfac-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6dfac-127">System.String</span></span>

## <span data-ttu-id="6dfac-128">출력</span><span class="sxs-lookup"><span data-stu-id="6dfac-128">OUTPUTS</span></span>

### <span data-ttu-id="6dfac-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="6dfac-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="6dfac-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6dfac-130">NOTES</span></span>

## <span data-ttu-id="6dfac-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6dfac-131">RELATED LINKS</span></span>
