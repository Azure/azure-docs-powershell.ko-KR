---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 471baa126cd58bb241fa6b8da358769d09be3f20
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048455"
---
# <span data-ttu-id="609f8-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="609f8-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="609f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="609f8-102">SYNOPSIS</span></span>
<span data-ttu-id="609f8-103">VMSS에 WinRM 수신기를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="609f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="609f8-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="609f8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="609f8-105">DESCRIPTION</span></span>
<span data-ttu-id="609f8-106">**AzVmssWinRMListener** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 WinRM (Windows Remote Management) 수신기를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="609f8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="609f8-107">EXAMPLES</span></span>

### <span data-ttu-id="609f8-108">예제 1: VMSS에 WinRM 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="609f8-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="609f8-109">이 예제에서는 VMSS에 WinRM 수신기를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="609f8-110">첫 번째 명령은 **AzVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="609f8-111">두 번째 명령은 지정 된 URL의 인증서가 있는 HTTP 프로토콜 WinRM 수신기를 VMSS에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="609f8-112">변수</span><span class="sxs-lookup"><span data-stu-id="609f8-112">PARAMETERS</span></span>

### <span data-ttu-id="609f8-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="609f8-113">-CertificateUrl</span></span>
<span data-ttu-id="609f8-114">새 가상 컴퓨터를 프로 비전 하는 데 사용할 인증서의 URL로 링크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="609f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609f8-115">-DefaultProfile</span></span>
<span data-ttu-id="609f8-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="609f8-117">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="609f8-117">-Protocol</span></span>
<span data-ttu-id="609f8-118">WinRM 수신기의 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="609f8-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="609f8-120">Http</span><span class="sxs-lookup"><span data-stu-id="609f8-120">Http</span></span>
- <span data-ttu-id="609f8-121">Https</span><span class="sxs-lookup"><span data-stu-id="609f8-121">Https</span></span>

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

### <span data-ttu-id="609f8-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="609f8-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="609f8-123">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="609f8-124">New-AzVmssConfig cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="609f8-125">-확인</span><span class="sxs-lookup"><span data-stu-id="609f8-125">-Confirm</span></span>
<span data-ttu-id="609f8-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="609f8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="609f8-127">-WhatIf</span></span>
<span data-ttu-id="609f8-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="609f8-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="609f8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609f8-130">CommonParameters</span></span>
<span data-ttu-id="609f8-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="609f8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609f8-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="609f8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609f8-133">입력</span><span class="sxs-lookup"><span data-stu-id="609f8-133">INPUTS</span></span>

### <span data-ttu-id="609f8-134">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="609f8-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="609f8-135">시스템 Null 허용 ' 1 [[23.0.0.0 형식, Microsoft Azure. Management. 관리., Version = 31bf3856ad364e35, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="609f8-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="609f8-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="609f8-136">System.String</span></span>

## <span data-ttu-id="609f8-137">출력</span><span class="sxs-lookup"><span data-stu-id="609f8-137">OUTPUTS</span></span>

### <span data-ttu-id="609f8-138">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="609f8-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="609f8-139">상속자</span><span class="sxs-lookup"><span data-stu-id="609f8-139">NOTES</span></span>

## <span data-ttu-id="609f8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="609f8-140">RELATED LINKS</span></span>

[<span data-ttu-id="609f8-141">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="609f8-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


