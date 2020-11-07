---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 662304cff991da0d9ffe9d946e63bc94ba51e4a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880473"
---
# <span data-ttu-id="03a12-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="03a12-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="03a12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03a12-102">SYNOPSIS</span></span>
<span data-ttu-id="03a12-103">키 자격 증명 모음에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03a12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03a12-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03a12-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03a12-105">DESCRIPTION</span></span>
<span data-ttu-id="03a12-106">**AzureKeyVaultCertificate** cmdlet은 키 자격 증명 모음에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="03a12-107">예제의</span><span class="sxs-lookup"><span data-stu-id="03a12-107">EXAMPLES</span></span>

### <span data-ttu-id="03a12-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="03a12-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="03a12-109">이 명령은 ContosoKV01 이라는 키 자격 증명 모음에서 SelfSigned01 이라는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="03a12-110">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="03a12-111">따라서 cmdlet에서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="03a12-112">예제 3: 키 자격 증명 모음에서 삭제 된 인증서 영구 제거</span><span class="sxs-lookup"><span data-stu-id="03a12-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="03a12-113">이 명령은 ' Contoso ' 라는 키 자격 증명 모음에서 ' MyCert ' 인증서를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="03a12-114">이 cmdlet을 실행 하려면 ' 제거 ' 권한이 필요 하며,이는 이전에이 키 보관소의 사용자에 게 명시적으로 부여 된 것 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="03a12-115">변수</span><span class="sxs-lookup"><span data-stu-id="03a12-115">PARAMETERS</span></span>

### <span data-ttu-id="03a12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a12-116">-DefaultProfile</span></span>
<span data-ttu-id="03a12-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="03a12-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03a12-118">-Force</span><span class="sxs-lookup"><span data-stu-id="03a12-118">-Force</span></span>
<span data-ttu-id="03a12-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03a12-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="03a12-120">-InRemovedState</span></span>
<span data-ttu-id="03a12-121">있는 경우 이전에 삭제 된 인증서를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-121">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="03a12-122">-이름</span><span class="sxs-lookup"><span data-stu-id="03a12-122">-Name</span></span>
<span data-ttu-id="03a12-123">이 cmdlet이 키 자격 증명 모음에서 제거할 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="03a12-124">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 인증서의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a12-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03a12-125">-PassThru</span></span>
<span data-ttu-id="03a12-126">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03a12-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03a12-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="03a12-128">-VaultName</span></span>
<span data-ttu-id="03a12-129">이 cmdlet이 인증서를 제거할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="03a12-130">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="03a12-131">-확인</span><span class="sxs-lookup"><span data-stu-id="03a12-131">-Confirm</span></span>
<span data-ttu-id="03a12-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03a12-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a12-133">-WhatIf</span></span>
<span data-ttu-id="03a12-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03a12-135">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03a12-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03a12-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a12-137">CommonParameters</span></span>
<span data-ttu-id="03a12-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03a12-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a12-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03a12-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a12-140">입력</span><span class="sxs-lookup"><span data-stu-id="03a12-140">INPUTS</span></span>

## <span data-ttu-id="03a12-141">출력</span><span class="sxs-lookup"><span data-stu-id="03a12-141">OUTPUTS</span></span>

### <span data-ttu-id="03a12-142">Microsoft. KeyVault.-모델-CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="03a12-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="03a12-143">상속자</span><span class="sxs-lookup"><span data-stu-id="03a12-143">NOTES</span></span>

## <span data-ttu-id="03a12-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03a12-144">RELATED LINKS</span></span>

[<span data-ttu-id="03a12-145">추가-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="03a12-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="03a12-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="03a12-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="03a12-147">가져오기-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="03a12-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="03a12-148">실행 취소-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="03a12-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
