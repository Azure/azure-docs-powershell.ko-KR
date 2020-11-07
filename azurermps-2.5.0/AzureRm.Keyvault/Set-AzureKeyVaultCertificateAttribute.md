---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
ms.openlocfilehash: 9f7c08f42026c6cc5d321ae78687a903c8393904
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880421"
---
# <span data-ttu-id="4c8f2-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="4c8f2-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="4c8f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="4c8f2-103">인증서의 편집 가능한 특성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c8f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c8f2-104">SYNTAX</span></span>

```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c8f2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4c8f2-105">DESCRIPTION</span></span>
<span data-ttu-id="4c8f2-106">**Set-AzureKeyVaultCertificateAttribute** cmdlet은 인증서의 편집 가능한 특성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-106">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="4c8f2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4c8f2-107">EXAMPLES</span></span>

### <span data-ttu-id="4c8f2-108">예제 1: 인증서와 연결 된 태그 수정</span><span class="sxs-lookup"><span data-stu-id="4c8f2-108">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="4c8f2-109">첫 번째 명령은 $Tags 변수에 키/값 쌍의 배열을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="4c8f2-110">두 번째 명령은 TestCert01 이라는 인증서의 태그 값을 $Tags 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="4c8f2-111">마지막 명령은 Get-AzureKeyVaultCertificate cmdlet을 사용 하 여 작업을 확인 하 여 TestCert01 인증서를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-111">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="4c8f2-112">변수</span><span class="sxs-lookup"><span data-stu-id="4c8f2-112">PARAMETERS</span></span>

### <span data-ttu-id="4c8f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c8f2-113">-DefaultProfile</span></span>
<span data-ttu-id="4c8f2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4c8f2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f2-115">-사용</span><span class="sxs-lookup"><span data-stu-id="4c8f2-115">-Enable</span></span>
<span data-ttu-id="4c8f2-116">인증서를 사용 하거나 사용 하지 않도록 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-116">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="4c8f2-117">사용 $False 하거나 사용 하지 않을 $True를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-117">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f2-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4c8f2-118">-Name</span></span>
<span data-ttu-id="4c8f2-119">수정할 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-119">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="4c8f2-120">이 cmdlet은 키 자격 증명 이름, 현재 선택 된 환경, 인증서 이름, 인증서 버전을 기반으로 인증서의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-120">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c8f2-121">-PassThru</span></span>
<span data-ttu-id="4c8f2-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4c8f2-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f2-124">태그</span><span class="sxs-lookup"><span data-stu-id="4c8f2-124">-Tag</span></span>
<span data-ttu-id="4c8f2-125">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4c8f2-126">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="4c8f2-126">For example:</span></span>

<span data-ttu-id="4c8f2-127">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4c8f2-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f2-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4c8f2-128">-VaultName</span></span>
<span data-ttu-id="4c8f2-129">이 cmdlet이 인증서를 수정할 키 보관소 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-129">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="4c8f2-130">이 cmdlet은 이름 및 현재 선택 된 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-130">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f2-131">-버전</span><span class="sxs-lookup"><span data-stu-id="4c8f2-131">-Version</span></span>
<span data-ttu-id="4c8f2-132">인증서의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-132">Specifies the version of a certificate.</span></span>
<span data-ttu-id="4c8f2-133">이 cmdlet은 키 자격 증명 이름, 현재 선택 된 환경, 인증서 이름, 인증서 버전을 기반으로 인증서의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-133">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c8f2-134">-확인</span><span class="sxs-lookup"><span data-stu-id="4c8f2-134">-Confirm</span></span>
<span data-ttu-id="4c8f2-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c8f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c8f2-136">-WhatIf</span></span>
<span data-ttu-id="4c8f2-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c8f2-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c8f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c8f2-139">CommonParameters</span></span>
<span data-ttu-id="4c8f2-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c8f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c8f2-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c8f2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c8f2-142">입력</span><span class="sxs-lookup"><span data-stu-id="4c8f2-142">INPUTS</span></span>

## <span data-ttu-id="4c8f2-143">출력</span><span class="sxs-lookup"><span data-stu-id="4c8f2-143">OUTPUTS</span></span>

### <span data-ttu-id="4c8f2-144">Microsoft. KeyVault. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4c8f2-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="4c8f2-145">상속자</span><span class="sxs-lookup"><span data-stu-id="4c8f2-145">NOTES</span></span>

## <span data-ttu-id="4c8f2-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c8f2-146">RELATED LINKS</span></span>

[<span data-ttu-id="4c8f2-147">추가-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4c8f2-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
