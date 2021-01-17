---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340077"
---
# <span data-ttu-id="8790b-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="8790b-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="8790b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8790b-102">SYNOPSIS</span></span>
<span data-ttu-id="8790b-103">VMSS의 네트워크 인터페이스에 대한 IP 태그 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8790b-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="8790b-104">구문</span><span class="sxs-lookup"><span data-stu-id="8790b-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8790b-105">설명</span><span class="sxs-lookup"><span data-stu-id="8790b-105">DESCRIPTION</span></span>
<span data-ttu-id="8790b-106">**New-AzVmssIpTagConfig** cmdlet은 VMSS(Virtual Machine Scale Set)의 네트워크 인터페이스에 대한 IP 태그 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8790b-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="8790b-107">이 cmdlet의 구성을 New-AzVmssIpConfig cmdlet의 *IPTag* 매개 변수로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8790b-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="8790b-108">예제</span><span class="sxs-lookup"><span data-stu-id="8790b-108">EXAMPLES</span></span>

### <span data-ttu-id="8790b-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="8790b-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="8790b-110">이 명령은 'FirstPartyUsage' 형식 및 'Sql' 태그를 사용하여 IP 태그 로컬 개체를 만든 다음, 이 IP 태그를 사용하여 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8790b-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="8790b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8790b-111">PARAMETERS</span></span>

### <span data-ttu-id="8790b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8790b-112">-DefaultProfile</span></span>
<span data-ttu-id="8790b-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8790b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8790b-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="8790b-114">-IpTagType</span></span>
<span data-ttu-id="8790b-115">IP 태그 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8790b-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="8790b-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="8790b-116">-Tag</span></span>
<span data-ttu-id="8790b-117">IP 태그 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8790b-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="8790b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8790b-118">-Confirm</span></span>
<span data-ttu-id="8790b-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8790b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8790b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8790b-120">-WhatIf</span></span>
<span data-ttu-id="8790b-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8790b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8790b-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8790b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8790b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8790b-123">CommonParameters</span></span>
<span data-ttu-id="8790b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8790b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8790b-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8790b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8790b-126">입력</span><span class="sxs-lookup"><span data-stu-id="8790b-126">INPUTS</span></span>

### <span data-ttu-id="8790b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8790b-127">System.String</span></span>

## <span data-ttu-id="8790b-128">출력</span><span class="sxs-lookup"><span data-stu-id="8790b-128">OUTPUTS</span></span>

### <span data-ttu-id="8790b-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="8790b-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="8790b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8790b-130">NOTES</span></span>

## <span data-ttu-id="8790b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8790b-131">RELATED LINKS</span></span>
