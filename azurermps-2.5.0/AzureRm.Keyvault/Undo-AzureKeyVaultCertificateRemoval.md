---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
ms.openlocfilehash: 493d4bcd641e8132bffd49100a04732759ce7e91
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881521"
---
# <span data-ttu-id="b6dbf-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="b6dbf-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="b6dbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="b6dbf-103">키 자격 증명 모음에서 삭제 된 인증서를 활성 상태로 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6dbf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6dbf-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6dbf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b6dbf-105">DESCRIPTION</span></span>
<span data-ttu-id="b6dbf-106">AzureKeyVaultCertificateRemoval cmdlet을 **실행** 하면 이전에 삭제 된 인증서가 복구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="b6dbf-107">복구 된 인증서는 활성화 되며 모든 작업에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="b6dbf-108">이 작업을 수행 하려면 호출자에 게 ' 복구 ' 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b6dbf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b6dbf-109">EXAMPLES</span></span>

### <span data-ttu-id="b6dbf-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6dbf-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="b6dbf-111">이 명령을 사용 하면 이전에 삭제 된 인증서 ' MyCertificate '을 활성 및 사용 가능한 상태로 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b6dbf-112">변수</span><span class="sxs-lookup"><span data-stu-id="b6dbf-112">PARAMETERS</span></span>

### <span data-ttu-id="b6dbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6dbf-113">-DefaultProfile</span></span>
<span data-ttu-id="b6dbf-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b6dbf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6dbf-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b6dbf-115">-Name</span></span>
<span data-ttu-id="b6dbf-116">인증서 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-116">Certificate name.</span></span>
<span data-ttu-id="b6dbf-117">Cmdlet은 자격 증명 이름, 현재 선택 된 환경 및 인증서 이름 으로부터 인증서의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="b6dbf-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b6dbf-118">-VaultName</span></span>
<span data-ttu-id="b6dbf-119">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="b6dbf-119">Vault name.</span></span>
<span data-ttu-id="b6dbf-120">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b6dbf-121">-확인</span><span class="sxs-lookup"><span data-stu-id="b6dbf-121">-Confirm</span></span>
<span data-ttu-id="b6dbf-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6dbf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6dbf-123">-WhatIf</span></span>
<span data-ttu-id="b6dbf-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6dbf-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6dbf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6dbf-126">CommonParameters</span></span>
<span data-ttu-id="b6dbf-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6dbf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6dbf-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6dbf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6dbf-129">입력</span><span class="sxs-lookup"><span data-stu-id="b6dbf-129">INPUTS</span></span>

### <span data-ttu-id="b6dbf-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b6dbf-130">System.String</span></span>

## <span data-ttu-id="b6dbf-131">출력</span><span class="sxs-lookup"><span data-stu-id="b6dbf-131">OUTPUTS</span></span>

### <span data-ttu-id="b6dbf-132">Microsoft. KeyVault. \* 인증서</span><span class="sxs-lookup"><span data-stu-id="b6dbf-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="b6dbf-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b6dbf-133">NOTES</span></span>

## <span data-ttu-id="b6dbf-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6dbf-134">RELATED LINKS</span></span>

[<span data-ttu-id="b6dbf-135">제거-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b6dbf-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="b6dbf-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b6dbf-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
