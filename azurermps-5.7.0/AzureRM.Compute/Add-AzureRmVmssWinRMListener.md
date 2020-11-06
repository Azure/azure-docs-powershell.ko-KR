---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssWinRMListener.md
ms.openlocfilehash: d2ed576131ad2ff33ae7e5c7e5be091ca8f4a50e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525335"
---
# <span data-ttu-id="fcd96-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="fcd96-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="fcd96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcd96-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd96-103">VMSS에 WinRM 수신기를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcd96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcd96-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcd96-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fcd96-105">DESCRIPTION</span></span>
<span data-ttu-id="fcd96-106">**AzureRmVmssWinRMListener** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 WinRM (Windows Remote Management) 수신기를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="fcd96-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fcd96-107">EXAMPLES</span></span>

### <span data-ttu-id="fcd96-108">예제 1: VMSS에 WinRM 수신기 추가</span><span class="sxs-lookup"><span data-stu-id="fcd96-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="fcd96-109">이 예제에서는 VMSS에 WinRM 수신기를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="fcd96-110">첫 번째 명령은 **AzureRmVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="fcd96-111">두 번째 명령은 지정 된 URL의 인증서가 있는 HTTP 프로토콜 WinRM 수신기를 VMSS에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="fcd96-112">변수</span><span class="sxs-lookup"><span data-stu-id="fcd96-112">PARAMETERS</span></span>

### <span data-ttu-id="fcd96-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="fcd96-113">-CertificateUrl</span></span>
<span data-ttu-id="fcd96-114">새 가상 컴퓨터를 프로 비전 하는 데 사용할 인증서의 URL로 링크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd96-115">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="fcd96-115">-Protocol</span></span>
<span data-ttu-id="fcd96-116">WinRM 수신기의 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-116">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="fcd96-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fcd96-118">Http</span><span class="sxs-lookup"><span data-stu-id="fcd96-118">Http</span></span>
- <span data-ttu-id="fcd96-119">Https</span><span class="sxs-lookup"><span data-stu-id="fcd96-119">Https</span></span>

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd96-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fcd96-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fcd96-121">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="fcd96-122">New-AzureRmVmssConfig cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-122">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcd96-123">-확인</span><span class="sxs-lookup"><span data-stu-id="fcd96-123">-Confirm</span></span>
<span data-ttu-id="fcd96-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd96-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcd96-125">-WhatIf</span></span>
<span data-ttu-id="fcd96-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcd96-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcd96-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd96-128">CommonParameters</span></span>
<span data-ttu-id="fcd96-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd96-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcd96-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd96-131">입력</span><span class="sxs-lookup"><span data-stu-id="fcd96-131">INPUTS</span></span>

### <span data-ttu-id="fcd96-132">않아야</span><span class="sxs-lookup"><span data-stu-id="fcd96-132">None</span></span>
<span data-ttu-id="fcd96-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fcd96-134">출력</span><span class="sxs-lookup"><span data-stu-id="fcd96-134">OUTPUTS</span></span>

### <span data-ttu-id="fcd96-135">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcd96-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="fcd96-136">상속자</span><span class="sxs-lookup"><span data-stu-id="fcd96-136">NOTES</span></span>

## <span data-ttu-id="fcd96-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcd96-137">RELATED LINKS</span></span>

[<span data-ttu-id="fcd96-138">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fcd96-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


