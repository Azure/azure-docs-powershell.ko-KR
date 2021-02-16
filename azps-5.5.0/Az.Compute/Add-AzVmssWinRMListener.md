---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 471baa126cd58bb241fa6b8da358769d09be3f20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195081"
---
# <span data-ttu-id="17878-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="17878-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="17878-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17878-102">SYNOPSIS</span></span>
<span data-ttu-id="17878-103">VMSS에 WinRM 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="17878-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="17878-104">구문</span><span class="sxs-lookup"><span data-stu-id="17878-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17878-105">설명</span><span class="sxs-lookup"><span data-stu-id="17878-105">DESCRIPTION</span></span>
<span data-ttu-id="17878-106">**Add-AzVmssWinRMListener** cmdlet은 VMSS(Virtual Machine Scale Set)에 WinRM(Windows 원격 관리) 수신기가 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="17878-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="17878-107">예제</span><span class="sxs-lookup"><span data-stu-id="17878-107">EXAMPLES</span></span>

### <span data-ttu-id="17878-108">예제 1: VMSS에 WinRM 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="17878-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="17878-109">이 예제에서는 VMSS에 WinRM 수신기 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="17878-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="17878-110">첫 번째 명령은 **New-AzVmssConfig** cmdlet을 사용하여 VMSS 구성 개체를 만들고 결과를 VMSS라는 이름의 변수에 $VMSS.</span><span class="sxs-lookup"><span data-stu-id="17878-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="17878-111">두 번째 명령은 지정된 URL에서 인증서를 사용하여 HTTP 프로토콜 WinRM 수신기를 VMSS에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="17878-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="17878-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17878-112">PARAMETERS</span></span>

### <span data-ttu-id="17878-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="17878-113">-CertificateUrl</span></span>
<span data-ttu-id="17878-114">새 가상 머신이 프로비전되는 인증서의 링크를 URL로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17878-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="17878-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17878-115">-DefaultProfile</span></span>
<span data-ttu-id="17878-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17878-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17878-117">-Protocol</span><span class="sxs-lookup"><span data-stu-id="17878-117">-Protocol</span></span>
<span data-ttu-id="17878-118">WinRM 수신기 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17878-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="17878-119">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="17878-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17878-120">Http</span><span class="sxs-lookup"><span data-stu-id="17878-120">Http</span></span>
- <span data-ttu-id="17878-121">Https</span><span class="sxs-lookup"><span data-stu-id="17878-121">Https</span></span>

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

### <span data-ttu-id="17878-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17878-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="17878-123">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17878-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="17878-124">New-AzVmssConfig cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17878-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="17878-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17878-125">-Confirm</span></span>
<span data-ttu-id="17878-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="17878-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17878-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17878-127">-WhatIf</span></span>
<span data-ttu-id="17878-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="17878-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17878-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17878-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17878-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17878-130">CommonParameters</span></span>
<span data-ttu-id="17878-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17878-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17878-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17878-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17878-133">입력</span><span class="sxs-lookup"><span data-stu-id="17878-133">INPUTS</span></span>

### <span data-ttu-id="17878-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17878-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="17878-135">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="17878-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="17878-136">System.String</span><span class="sxs-lookup"><span data-stu-id="17878-136">System.String</span></span>

## <span data-ttu-id="17878-137">출력</span><span class="sxs-lookup"><span data-stu-id="17878-137">OUTPUTS</span></span>

### <span data-ttu-id="17878-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17878-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="17878-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17878-139">NOTES</span></span>

## <span data-ttu-id="17878-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17878-140">RELATED LINKS</span></span>

[<span data-ttu-id="17878-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="17878-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


