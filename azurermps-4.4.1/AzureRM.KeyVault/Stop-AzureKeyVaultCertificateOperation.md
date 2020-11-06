---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3B042D79-658F-41F0-BD4D-9955F2E71CA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Stop-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Stop-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: b413c71deb70081689c2870e95c71a0ad14a1928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536328"
---
# <span data-ttu-id="ab07c-101">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="ab07c-101">Stop-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="ab07c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab07c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab07c-103">키 자격 증명 모음에서 인증서 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-103">Cancels a certificate operation in key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab07c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab07c-104">SYNTAX</span></span>

```
Stop-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab07c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab07c-105">DESCRIPTION</span></span>
<span data-ttu-id="ab07c-106">**AzureKeyVaultCertificateOperation** Cmdlet은 Azure 키 자격 증명 모음 서비스에서 인증서 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-106">The **Stop-AzureKeyVaultCertificateOperation** cmdlet cancels a certificate operation in the Azure Key Vault service.</span></span>

## <span data-ttu-id="ab07c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ab07c-107">EXAMPLES</span></span>

### <span data-ttu-id="ab07c-108">예제 1: 인증서 작업 취소</span><span class="sxs-lookup"><span data-stu-id="ab07c-108">Example 1: Cancel a certificate operation</span></span>
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

<span data-ttu-id="ab07c-109">이 명령은 TestCert02 certificate 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-109">This command cancels the TestCert02 certificate operation.</span></span>

## <span data-ttu-id="ab07c-110">변수</span><span class="sxs-lookup"><span data-stu-id="ab07c-110">PARAMETERS</span></span>

### <span data-ttu-id="ab07c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ab07c-111">-Force</span></span>
<span data-ttu-id="ab07c-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab07c-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ab07c-113">-Name</span></span>
<span data-ttu-id="ab07c-114">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-114">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab07c-115">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ab07c-115">-VaultName</span></span>
<span data-ttu-id="ab07c-116">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-116">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab07c-117">-확인</span><span class="sxs-lookup"><span data-stu-id="ab07c-117">-Confirm</span></span>
<span data-ttu-id="ab07c-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab07c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab07c-119">-WhatIf</span></span>
<span data-ttu-id="ab07c-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab07c-121">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-121">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab07c-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab07c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab07c-123">-DefaultProfile</span></span>
<span data-ttu-id="ab07c-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab07c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab07c-125">CommonParameters</span></span>
<span data-ttu-id="ab07c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab07c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab07c-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab07c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab07c-128">입력</span><span class="sxs-lookup"><span data-stu-id="ab07c-128">INPUTS</span></span>

## <span data-ttu-id="ab07c-129">출력</span><span class="sxs-lookup"><span data-stu-id="ab07c-129">OUTPUTS</span></span>

### <span data-ttu-id="ab07c-130">Microsoft. KeyVault. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="ab07c-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="ab07c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ab07c-131">NOTES</span></span>

## <span data-ttu-id="ab07c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab07c-132">RELATED LINKS</span></span>

[<span data-ttu-id="ab07c-133">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="ab07c-133">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="ab07c-134">제거-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="ab07c-134">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

