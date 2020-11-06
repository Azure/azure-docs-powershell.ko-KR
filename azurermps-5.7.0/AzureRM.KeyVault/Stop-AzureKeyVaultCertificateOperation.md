---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/stop-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Stop-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Stop-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: a7af611c4db4fb2e3e1c85c5726be31d2a87935f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532160"
---
# <span data-ttu-id="fc7ca-101">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="fc7ca-101">Stop-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="fc7ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7ca-103">키 자격 증명 모음에서 인증서 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-103">Cancels a certificate operation in key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc7ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc7ca-104">SYNTAX</span></span>

### <span data-ttu-id="fc7ca-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc7ca-105">Default (Default)</span></span>
```
Stop-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc7ca-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fc7ca-106">InputObject</span></span>
```
Stop-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc7ca-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fc7ca-107">DESCRIPTION</span></span>
<span data-ttu-id="fc7ca-108">**AzureKeyVaultCertificateOperation** Cmdlet은 Azure 키 자격 증명 모음 서비스에서 인증서 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-108">The **Stop-AzureKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="fc7ca-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fc7ca-109">EXAMPLES</span></span>

### <span data-ttu-id="fc7ca-110">예제 1: 인증서 작업 취소</span><span class="sxs-lookup"><span data-stu-id="fc7ca-110">Example 1: Cancel a certificate operation</span></span>
```
PS C:\>Stop-AzureKeyVaultCertificateOperation -VaultName "Contoso01" -Name "TestCert02" -Force
Status                    : inProgress
CancellationRequested     : True
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCVr6EVwsd48qDVORsF4V4w4N1aQCUirFW7b+kwoTvSOL4SfMiWcPmno0uxmQQoh
                            gz157bC3sKFLyBUsGCmS4i7uWkBOSEpCh8L3FKU4XMqRROlUM9AqswzB0e1sURCqevEJA80xFpfTgkeqpm44m4jr6p7gu+h1PBf9Dt7b43Gybde5DUlGrrOiTkOIAF0eU2iNVeHOapoj8m1XHmzO1BARs
                            oa0pSDxO/aMgeuq/QPkWG64Iiw55U20byKZ86u3Y4g192HsPwsrHkf9ZSYR2M9BYM3YGoT/dkCmAtP4LQAsOwf1+S0a/TwRtrnoOHbPFI6HYSY3TY1iqzZ9xItfgalAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAjxUX5PGhri9qJTxSleGEbMVkxhhn3nuPUgxujEzrcQVr
                            fZAACJHbOnga/QYwpxumKWnkX9YdWxb58PPn+nLV2gYP3eYEyJ4DR9XDcKpoQxZahUdqD3JZXhWPIcN05tw9Fuq8ziw94BjLZW3h3iDamqkBnysJYW58FBp1H8Ejqk0Iynbo0V223Innq/7QB2fVwe3ZJ
                            JecT8YxHJjVQ5psdDpEWgLUG/DFiAPHdwupI7JjvtvQmT3AotL0x5GNx2bWNH5hHIXsX4bnbxZgNQnTB2w3tQ3QeuKt8fUx2S0xtxPllaCUul6efa84TNqdMcMfyxCarIwDP6qdhS+CDU1uUA==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="fc7ca-111">이 명령은 TestCert02 certificate 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-111">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="fc7ca-112">변수</span><span class="sxs-lookup"><span data-stu-id="fc7ca-112">PARAMETERS</span></span>

### <span data-ttu-id="fc7ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7ca-113">-DefaultProfile</span></span>
<span data-ttu-id="fc7ca-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fc7ca-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc7ca-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fc7ca-115">-Force</span></span>
<span data-ttu-id="fc7ca-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc7ca-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc7ca-117">-InputObject</span></span>
<span data-ttu-id="fc7ca-118">작업 개체</span><span class="sxs-lookup"><span data-stu-id="fc7ca-118">Operation object</span></span>

```yaml
Type: PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7ca-119">-이름</span><span class="sxs-lookup"><span data-stu-id="fc7ca-119">-Name</span></span>
<span data-ttu-id="fc7ca-120">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-120">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7ca-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fc7ca-121">-VaultName</span></span>
<span data-ttu-id="fc7ca-122">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-122">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7ca-123">-확인</span><span class="sxs-lookup"><span data-stu-id="fc7ca-123">-Confirm</span></span>
<span data-ttu-id="fc7ca-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7ca-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc7ca-125">-WhatIf</span></span>
<span data-ttu-id="fc7ca-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc7ca-127">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-127">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc7ca-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc7ca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7ca-129">CommonParameters</span></span>
<span data-ttu-id="fc7ca-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7ca-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc7ca-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7ca-132">입력</span><span class="sxs-lookup"><span data-stu-id="fc7ca-132">INPUTS</span></span>

### <span data-ttu-id="fc7ca-133">않아야</span><span class="sxs-lookup"><span data-stu-id="fc7ca-133">None</span></span>
<span data-ttu-id="fc7ca-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc7ca-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fc7ca-135">출력</span><span class="sxs-lookup"><span data-stu-id="fc7ca-135">OUTPUTS</span></span>

### <span data-ttu-id="fc7ca-136">Microsoft. KeyVault. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="fc7ca-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="fc7ca-137">상속자</span><span class="sxs-lookup"><span data-stu-id="fc7ca-137">NOTES</span></span>

## <span data-ttu-id="fc7ca-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc7ca-138">RELATED LINKS</span></span>

[<span data-ttu-id="fc7ca-139">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="fc7ca-139">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="fc7ca-140">제거-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="fc7ca-140">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

