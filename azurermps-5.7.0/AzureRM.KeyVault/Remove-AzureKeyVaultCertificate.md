---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 6c8fcc5476ea2defda78ea03cc1acce7b7e3dea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534796"
---
# <span data-ttu-id="2770d-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2770d-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="2770d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2770d-102">SYNOPSIS</span></span>
<span data-ttu-id="2770d-103">키 자격 증명 모음에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2770d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2770d-104">SYNTAX</span></span>

### <span data-ttu-id="2770d-105">ByVaultNameAndName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2770d-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2770d-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="2770d-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2770d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2770d-107">DESCRIPTION</span></span>
<span data-ttu-id="2770d-108">**AzureKeyVaultCertificate** cmdlet은 키 자격 증명 모음에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-108">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="2770d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2770d-109">EXAMPLES</span></span>

### <span data-ttu-id="2770d-110">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="2770d-110">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="2770d-111">이 명령은 ContosoKV01 이라는 키 자격 증명 모음에서 SelfSigned01 이라는 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="2770d-112">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2770d-113">따라서 cmdlet에서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="2770d-114">예제 3: 키 자격 증명 모음에서 삭제 된 인증서 영구 제거</span><span class="sxs-lookup"><span data-stu-id="2770d-114">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="2770d-115">이 명령은 ' Contoso ' 라는 키 자격 증명 모음에서 ' MyCert ' 인증서를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="2770d-116">이 cmdlet을 실행 하려면 ' 제거 ' 권한이 필요 하며,이는 이전에이 키 보관소의 사용자에 게 명시적으로 부여 된 것 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="2770d-117">변수</span><span class="sxs-lookup"><span data-stu-id="2770d-117">PARAMETERS</span></span>

### <span data-ttu-id="2770d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2770d-118">-DefaultProfile</span></span>
<span data-ttu-id="2770d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2770d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2770d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2770d-120">-Force</span></span>
<span data-ttu-id="2770d-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2770d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2770d-122">-InputObject</span></span>
<span data-ttu-id="2770d-123">인증서 개체.</span><span class="sxs-lookup"><span data-stu-id="2770d-123">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2770d-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="2770d-124">-InRemovedState</span></span>
<span data-ttu-id="2770d-125">있는 경우 이전에 삭제 된 인증서를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="2770d-126">-이름</span><span class="sxs-lookup"><span data-stu-id="2770d-126">-Name</span></span>
<span data-ttu-id="2770d-127">이 cmdlet이 키 자격 증명 모음에서 제거할 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="2770d-128">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 인증서의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2770d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2770d-129">-PassThru</span></span>
<span data-ttu-id="2770d-130">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2770d-131">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2770d-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2770d-132">-VaultName</span></span>
<span data-ttu-id="2770d-133">이 cmdlet이 인증서를 제거할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="2770d-134">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2770d-135">-확인</span><span class="sxs-lookup"><span data-stu-id="2770d-135">-Confirm</span></span>
<span data-ttu-id="2770d-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2770d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2770d-137">-WhatIf</span></span>
<span data-ttu-id="2770d-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2770d-139">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2770d-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2770d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2770d-141">CommonParameters</span></span>
<span data-ttu-id="2770d-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2770d-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2770d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2770d-144">입력</span><span class="sxs-lookup"><span data-stu-id="2770d-144">INPUTS</span></span>

### <span data-ttu-id="2770d-145">않아야</span><span class="sxs-lookup"><span data-stu-id="2770d-145">None</span></span>
<span data-ttu-id="2770d-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2770d-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2770d-147">출력</span><span class="sxs-lookup"><span data-stu-id="2770d-147">OUTPUTS</span></span>

### <span data-ttu-id="2770d-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2770d-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="2770d-149">상속자</span><span class="sxs-lookup"><span data-stu-id="2770d-149">NOTES</span></span>

## <span data-ttu-id="2770d-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2770d-150">RELATED LINKS</span></span>

[<span data-ttu-id="2770d-151">추가-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2770d-151">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="2770d-152">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2770d-152">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="2770d-153">가져오기-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2770d-153">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="2770d-154">실행 취소-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="2770d-154">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
