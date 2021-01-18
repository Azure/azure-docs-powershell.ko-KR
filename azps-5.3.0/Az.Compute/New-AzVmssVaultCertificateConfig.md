---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 23b2b3acd5bb15771d3383cc39c6e0a69073a750
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496024"
---
# <span data-ttu-id="1f068-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="1f068-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="1f068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f068-102">SYNOPSIS</span></span>
<span data-ttu-id="1f068-103">Key Vault 인증서 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="1f068-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f068-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f068-105">설명</span><span class="sxs-lookup"><span data-stu-id="1f068-105">DESCRIPTION</span></span>
<span data-ttu-id="1f068-106">**New-AzVmssVaultCertificateConfig** cmdlet은 VMSS(Virtual Machine Scale Set) 가상 머신에 배치해야 하는 비밀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="1f068-107">이 cmdlet의 출력은 Add-AzVmssSecret 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="1f068-108">예제</span><span class="sxs-lookup"><span data-stu-id="1f068-108">EXAMPLES</span></span>

### <span data-ttu-id="1f068-109">예제 1: Key Vault 인증서 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="1f068-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="1f068-110">이 명령은 지정된 인증서 URL에 있는 MyCerts라는 인증서 저장소를 사용하는 Key Vault 인증서 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="1f068-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f068-111">PARAMETERS</span></span>

### <span data-ttu-id="1f068-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="1f068-112">-CertificateStore</span></span>
<span data-ttu-id="1f068-113">인증서가 추가되는 확장 집합의 가상 머신에 인증서 저장소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="1f068-114">이 설정은 Windows Virtual Machine Scale Sets에만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f068-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="1f068-115">-CertificateUrl</span></span>
<span data-ttu-id="1f068-116">Key Vault에 저장된 인증서의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="1f068-117">UTF-8로 인코딩된 다음 JSON 개체의 base64 인코딩입니다. { "data":" \<Base64-encoded-certificate\> ", "dataType":"pfx", "password":" \<pfx-file-password\> }</span><span class="sxs-lookup"><span data-stu-id="1f068-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f068-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f068-118">-DefaultProfile</span></span>
<span data-ttu-id="1f068-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f068-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f068-120">-Confirm</span></span>
<span data-ttu-id="1f068-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f068-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f068-122">-WhatIf</span></span>
<span data-ttu-id="1f068-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1f068-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f068-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f068-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f068-125">CommonParameters</span></span>
<span data-ttu-id="1f068-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f068-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f068-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f068-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f068-128">입력</span><span class="sxs-lookup"><span data-stu-id="1f068-128">INPUTS</span></span>

### <span data-ttu-id="1f068-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1f068-129">System.String</span></span>

## <span data-ttu-id="1f068-130">출력</span><span class="sxs-lookup"><span data-stu-id="1f068-130">OUTPUTS</span></span>

### <span data-ttu-id="1f068-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1f068-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="1f068-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f068-132">NOTES</span></span>

## <span data-ttu-id="1f068-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f068-133">RELATED LINKS</span></span>

[<span data-ttu-id="1f068-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="1f068-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
