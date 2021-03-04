---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 9e4c560021f03b2612d2b7d3bd60fd91a72aa53b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969472"
---
# <span data-ttu-id="ecd63-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="ecd63-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="ecd63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecd63-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd63-103">VMSS에 WinRM 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="ecd63-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="ecd63-104">구문</span><span class="sxs-lookup"><span data-stu-id="ecd63-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecd63-105">설명</span><span class="sxs-lookup"><span data-stu-id="ecd63-105">DESCRIPTION</span></span>
<span data-ttu-id="ecd63-106">**Add-AzVmssWinRMListener** cmdlet은 VMSS(Virtual Machine Scale Set)에 Windows 원격 관리(WinRM) 수신기가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ecd63-107">예제</span><span class="sxs-lookup"><span data-stu-id="ecd63-107">EXAMPLES</span></span>

### <span data-ttu-id="ecd63-108">예제 1: VMSS에 WinRM 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="ecd63-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="ecd63-109">이 예제에서는 VMSS에 WinRM 수신기 를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="ecd63-110">첫 번째 명령은 **New-AzVmssConfig** cmdlet을 사용하여 VMSS 구성 개체를 만들고 결과를 새 이름의 변수에 $VMSS.</span><span class="sxs-lookup"><span data-stu-id="ecd63-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="ecd63-111">두 번째 명령은 지정된 URL에서 인증서가 있는 HTTP 프로토콜 WinRM 수신기를 VMSS에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="ecd63-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ecd63-112">PARAMETERS</span></span>

### <span data-ttu-id="ecd63-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="ecd63-113">-CertificateUrl</span></span>
<span data-ttu-id="ecd63-114">새 가상 머신이 프로비전되는 인증서의 URL로 링크를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd63-115">-DefaultProfile</span></span>
<span data-ttu-id="ecd63-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecd63-117">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ecd63-117">-Protocol</span></span>
<span data-ttu-id="ecd63-118">WinRM 수신기 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="ecd63-119">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ecd63-120">Http</span><span class="sxs-lookup"><span data-stu-id="ecd63-120">Http</span></span>
- <span data-ttu-id="ecd63-121">Https</span><span class="sxs-lookup"><span data-stu-id="ecd63-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd63-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ecd63-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ecd63-123">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="ecd63-124">New-AzVmssConfig cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd63-125">-확인</span><span class="sxs-lookup"><span data-stu-id="ecd63-125">-Confirm</span></span>
<span data-ttu-id="ecd63-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd63-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd63-127">-WhatIf</span></span>
<span data-ttu-id="ecd63-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecd63-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecd63-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd63-130">CommonParameters</span></span>
<span data-ttu-id="ecd63-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd63-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd63-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecd63-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd63-133">입력</span><span class="sxs-lookup"><span data-stu-id="ecd63-133">INPUTS</span></span>

### <span data-ttu-id="ecd63-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ecd63-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ecd63-135">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ecd63-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ecd63-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ecd63-136">System.String</span></span>

## <span data-ttu-id="ecd63-137">출력</span><span class="sxs-lookup"><span data-stu-id="ecd63-137">OUTPUTS</span></span>

### <span data-ttu-id="ecd63-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ecd63-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ecd63-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ecd63-139">NOTES</span></span>

## <span data-ttu-id="ecd63-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecd63-140">RELATED LINKS</span></span>

[<span data-ttu-id="ecd63-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ecd63-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


