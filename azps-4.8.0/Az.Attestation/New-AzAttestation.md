---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056810"
---
# <span data-ttu-id="b8f6b-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="b8f6b-101">New-AzAttestation</span></span>

## <span data-ttu-id="b8f6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f6b-103">증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-103">Creates an attestation</span></span>

## <span data-ttu-id="b8f6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8f6b-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8f6b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b8f6b-105">DESCRIPTION</span></span>
<span data-ttu-id="b8f6b-106">New-AzAttestation cmdlet은 지정 된 리소스 그룹에 증명을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="b8f6b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b8f6b-107">EXAMPLES</span></span>

### <span data-ttu-id="b8f6b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8f6b-108">Example 1</span></span>
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

<span data-ttu-id="b8f6b-109">두 개의 태그로 *pshtest4* 이라는 증명 공급자의 새 인스턴스를 만들고, 마스터링 티에 대 한 AAD 신뢰를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="b8f6b-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="b8f6b-110">Example 2</span></span>
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

<span data-ttu-id="b8f6b-111">PEM 파일을 통해 신뢰할 수 있는 서명 키 집합을 지정 하 여 Isoladed 신뢰를 사용 하는 *pshtest3* ' 라는 증명 공급자의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-111">Create a new instance of an Attestation Provider named *pshtest3* \` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="b8f6b-112">변수</span><span class="sxs-lookup"><span data-stu-id="b8f6b-112">PARAMETERS</span></span>

### <span data-ttu-id="b8f6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8f6b-113">-DefaultProfile</span></span>
<span data-ttu-id="b8f6b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8f6b-115">-위치</span><span class="sxs-lookup"><span data-stu-id="b8f6b-115">-Location</span></span>
<span data-ttu-id="b8f6b-116">증명 공급자를 만들 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="b8f6b-117">명령 Get-AzResourceProvider를 ProviderNamespace 매개 변수와 함께 사용 하 여 선택 항목을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="b8f6b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="b8f6b-118">-Name</span></span>
<span data-ttu-id="b8f6b-119">만들 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="b8f6b-120">이름은 문자, 숫자 또는 하이픈을 임의로 조합 하 여 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="b8f6b-121">이름은 문자 또는 숫자로 시작 하 고 끝나야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="b8f6b-122">이름은 범용으로 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-122">The name must be universally unique.</span></span>

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

### <span data-ttu-id="b8f6b-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="b8f6b-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="b8f6b-124">단일 인증서 파일의 발급 정책에 대 한 신뢰할 수 있는 서명 키 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

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

### <span data-ttu-id="b8f6b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8f6b-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8f6b-126">증명을 만들 기존 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

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

### <span data-ttu-id="b8f6b-127">태그</span><span class="sxs-lookup"><span data-stu-id="b8f6b-127">-Tag</span></span>
<span data-ttu-id="b8f6b-128">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b8f6b-129">-확인</span><span class="sxs-lookup"><span data-stu-id="b8f6b-129">-Confirm</span></span>
<span data-ttu-id="b8f6b-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8f6b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8f6b-131">-WhatIf</span></span>
<span data-ttu-id="b8f6b-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8f6b-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8f6b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f6b-134">CommonParameters</span></span>
<span data-ttu-id="b8f6b-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f6b-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b8f6b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f6b-137">입력</span><span class="sxs-lookup"><span data-stu-id="b8f6b-137">INPUTS</span></span>

### <span data-ttu-id="b8f6b-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8f6b-138">System.String</span></span>

### <span data-ttu-id="b8f6b-139">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="b8f6b-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b8f6b-140">출력</span><span class="sxs-lookup"><span data-stu-id="b8f6b-140">OUTPUTS</span></span>

### <span data-ttu-id="b8f6b-141">Microsoft. Azure. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="b8f6b-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="b8f6b-142">상속자</span><span class="sxs-lookup"><span data-stu-id="b8f6b-142">NOTES</span></span>

## <span data-ttu-id="b8f6b-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8f6b-143">RELATED LINKS</span></span>
