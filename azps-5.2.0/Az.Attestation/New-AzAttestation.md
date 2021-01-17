---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353318"
---
# <span data-ttu-id="81012-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="81012-101">New-AzAttestation</span></span>

## <span data-ttu-id="81012-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81012-102">SYNOPSIS</span></span>
<span data-ttu-id="81012-103">Attestation을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81012-103">Creates an attestation</span></span>

## <span data-ttu-id="81012-104">구문</span><span class="sxs-lookup"><span data-stu-id="81012-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81012-105">설명</span><span class="sxs-lookup"><span data-stu-id="81012-105">DESCRIPTION</span></span>
<span data-ttu-id="81012-106">이 New-AzAttestation cmdlet은 지정된 리소스 그룹에 대한 토의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81012-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="81012-107">예제</span><span class="sxs-lookup"><span data-stu-id="81012-107">EXAMPLES</span></span>

### <span data-ttu-id="81012-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="81012-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

<span data-ttu-id="81012-109">몇 가지 태그와 TEE 정책 마스터에 AAD 트러스트를 사용하여 *pshtest4라는 Attestation* Provider의 새 인스턴스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81012-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="81012-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="81012-110">Example 2</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="81012-111">PEM 파일을 통해 신뢰할 수 있는 서명 키 집합을 지정하여 TEE 정책을 마스터하는 데 Isoladed 트러스트를 사용하는 *pshtest3'이라는 Attestation* Provider의 새 인스턴스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81012-111">Create a new instance of an Attestation Provider named *pshtest3*\` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="81012-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81012-112">PARAMETERS</span></span>

### <span data-ttu-id="81012-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81012-113">-DefaultProfile</span></span>
<span data-ttu-id="81012-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81012-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81012-115">-Location</span><span class="sxs-lookup"><span data-stu-id="81012-115">-Location</span></span>
<span data-ttu-id="81012-116">등록 공급자를 만들 Azure 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="81012-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="81012-117">ProviderNamespace Get-AzResourceProvider 명령을 사용하여 선택을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81012-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81012-118">-Name</span><span class="sxs-lookup"><span data-stu-id="81012-118">-Name</span></span>
<span data-ttu-id="81012-119">만들 인스턴스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="81012-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="81012-120">이름은 문자, 숫자 또는 하이픈의 조합일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81012-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="81012-121">이름은 문자 또는 숫자로 시작하고 끝나야 합니다.</span><span class="sxs-lookup"><span data-stu-id="81012-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="81012-122">이름은 범용적으로 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="81012-122">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81012-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="81012-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="81012-124">단일 인증서 파일에서 발급 정책에 대한 신뢰할 수 있는 서명 키 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="81012-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

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

### <span data-ttu-id="81012-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81012-125">-ResourceGroupName</span></span>
<span data-ttu-id="81012-126">토의를 만들 기존 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="81012-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81012-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="81012-127">-Tag</span></span>
<span data-ttu-id="81012-128">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="81012-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81012-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81012-129">-Confirm</span></span>
<span data-ttu-id="81012-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="81012-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81012-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81012-131">-WhatIf</span></span>
<span data-ttu-id="81012-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="81012-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81012-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81012-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81012-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81012-134">CommonParameters</span></span>
<span data-ttu-id="81012-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="81012-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81012-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="81012-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81012-137">입력</span><span class="sxs-lookup"><span data-stu-id="81012-137">INPUTS</span></span>

### <span data-ttu-id="81012-138">System.String</span><span class="sxs-lookup"><span data-stu-id="81012-138">System.String</span></span>

### <span data-ttu-id="81012-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="81012-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="81012-140">출력</span><span class="sxs-lookup"><span data-stu-id="81012-140">OUTPUTS</span></span>

### <span data-ttu-id="81012-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="81012-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="81012-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="81012-142">NOTES</span></span>

## <span data-ttu-id="81012-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81012-143">RELATED LINKS</span></span>
