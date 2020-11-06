---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultCertificate.md
ms.openlocfilehash: 732d8dc7cfe3c0f8a3bec6eb3157b65bc8437e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530254"
---
# <span data-ttu-id="6d00f-101">Update-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6d00f-101">Update-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="6d00f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d00f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d00f-103">인증서의 편집 가능한 특성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d00f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d00f-104">SYNTAX</span></span>

### <span data-ttu-id="6d00f-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6d00f-105">ByName (Default)</span></span>
```
Update-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d00f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6d00f-106">ByInputObject</span></span>
```
Update-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d00f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6d00f-107">DESCRIPTION</span></span>
<span data-ttu-id="6d00f-108">**업데이트 AzureKeyVaultCertificate** cmdlet은 인증서의 편집 가능한 특성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-108">The **Update-AzureKeyVaultCertificate** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="6d00f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6d00f-109">EXAMPLES</span></span>

### <span data-ttu-id="6d00f-110">예제 1: 인증서와 연결 된 태그 수정</span><span class="sxs-lookup"><span data-stu-id="6d00f-110">Example 1: Modify the tags associated with a certificate</span></span>
```powershell
PS C:\> $Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Update-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags -PassThru

Name        : TestCert01
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Id          : https://ContosoKV01.vault.azure.net:443/certificates/TestCert01
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/TestCert01
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/TestCert01
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="6d00f-111">첫 번째 명령은 $Tags 변수에 키/값 쌍의 배열을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-111">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="6d00f-112">두 번째 명령은 TestCert01 이라는 인증서의 태그 값을 $Tags 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-112">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

## <span data-ttu-id="6d00f-113">변수</span><span class="sxs-lookup"><span data-stu-id="6d00f-113">PARAMETERS</span></span>

### <span data-ttu-id="6d00f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d00f-114">-DefaultProfile</span></span>
<span data-ttu-id="6d00f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-116">-사용</span><span class="sxs-lookup"><span data-stu-id="6d00f-116">-Enable</span></span>
<span data-ttu-id="6d00f-117">있는 경우 값이 true 이면 인증서를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-117">If present, enable a certificate if value is true.</span></span>
<span data-ttu-id="6d00f-118">값이 false 이면 인증서를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-118">Disable a certificate if value is false.</span></span>
<span data-ttu-id="6d00f-119">지정 하지 않으면 인증서의 사용/사용 안 함 상태에 대 한 기존 값이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-119">If not specified, the existing value of the certificate's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d00f-120">-InputObject</span></span>
<span data-ttu-id="6d00f-121">인증서 개체</span><span class="sxs-lookup"><span data-stu-id="6d00f-121">Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-122">-이름</span><span class="sxs-lookup"><span data-stu-id="6d00f-122">-Name</span></span>
<span data-ttu-id="6d00f-123">인증서 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-123">Certificate name.</span></span>
<span data-ttu-id="6d00f-124">Cmdlet은 자격 증명 정보, 현재 선택 된 환경 및 비밀 이름 으로부터 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-124">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d00f-125">-PassThru</span></span>
<span data-ttu-id="6d00f-126">Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-126">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="6d00f-127">이 스위치가 지정 된 경우 certificate 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-127">If this switch is specified, return certificate object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-128">태그</span><span class="sxs-lookup"><span data-stu-id="6d00f-128">-Tag</span></span>
<span data-ttu-id="6d00f-129">인증서 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-129">A hashtable representing certificate tags.</span></span>
<span data-ttu-id="6d00f-130">지정 하지 않은 경우 sertificate의 기존 태그는 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-130">If not specified, the existing tags of the sertificate remain unchanged.</span></span>
<span data-ttu-id="6d00f-131">빈 Hashtable을 지정 하 여 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-131">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6d00f-132">-VaultName</span></span>
<span data-ttu-id="6d00f-133">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="6d00f-133">Vault name.</span></span>
<span data-ttu-id="6d00f-134">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-134">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-135">-버전</span><span class="sxs-lookup"><span data-stu-id="6d00f-135">-Version</span></span>
<span data-ttu-id="6d00f-136">인증서 버전.</span><span class="sxs-lookup"><span data-stu-id="6d00f-136">Certificate version.</span></span>
<span data-ttu-id="6d00f-137">Cmdlet은 자격 증명 모음 이름, 현재 선택 된 환경, 인증서 이름, 인증서 버전 으로부터 인증서의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-137">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment, certificate name and certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d00f-138">-확인</span><span class="sxs-lookup"><span data-stu-id="6d00f-138">-Confirm</span></span>
<span data-ttu-id="6d00f-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d00f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d00f-140">-WhatIf</span></span>
<span data-ttu-id="6d00f-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d00f-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d00f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d00f-143">CommonParameters</span></span>
<span data-ttu-id="6d00f-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d00f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d00f-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d00f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d00f-146">입력</span><span class="sxs-lookup"><span data-stu-id="6d00f-146">INPUTS</span></span>

### <span data-ttu-id="6d00f-147">Microsoft. KeyVault. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6d00f-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="6d00f-148">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d00f-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6d00f-149">출력</span><span class="sxs-lookup"><span data-stu-id="6d00f-149">OUTPUTS</span></span>

### <span data-ttu-id="6d00f-150">Microsoft. KeyVault. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="6d00f-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="6d00f-151">상속자</span><span class="sxs-lookup"><span data-stu-id="6d00f-151">NOTES</span></span>

## <span data-ttu-id="6d00f-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d00f-152">RELATED LINKS</span></span>
