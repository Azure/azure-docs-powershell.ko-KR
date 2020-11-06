---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 70d6d39ed3e2083bf0f52e9e56808b7d36f1cc24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529806"
---
# <span data-ttu-id="72280-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="72280-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="72280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72280-102">SYNOPSIS</span></span>
<span data-ttu-id="72280-103">키 자격 증명 모음에서 인증서 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="72280-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72280-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72280-104">SYNTAX</span></span>

### <span data-ttu-id="72280-105">기본값</span><span class="sxs-lookup"><span data-stu-id="72280-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72280-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="72280-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72280-107">설명은</span><span class="sxs-lookup"><span data-stu-id="72280-107">DESCRIPTION</span></span>
<span data-ttu-id="72280-108">**AzureKeyVaultCertificateOperation** cmdlet은 키 자격 증명 모음에서 인증서 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="72280-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="72280-109">예제의</span><span class="sxs-lookup"><span data-stu-id="72280-109">EXAMPLES</span></span>

### <span data-ttu-id="72280-110">예제 1: 인증서 작업 제거</span><span class="sxs-lookup"><span data-stu-id="72280-110">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="72280-111">이 명령은 확인 메시지를 표시 하지 않고 ContosoKV01 키 자격 증명 모음에서 TestCert01 이라는 인증서 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="72280-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="72280-112">변수</span><span class="sxs-lookup"><span data-stu-id="72280-112">PARAMETERS</span></span>

### <span data-ttu-id="72280-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72280-113">-DefaultProfile</span></span>
<span data-ttu-id="72280-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="72280-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72280-115">-Force</span><span class="sxs-lookup"><span data-stu-id="72280-115">-Force</span></span>
<span data-ttu-id="72280-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="72280-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72280-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72280-117">-InputObject</span></span>
<span data-ttu-id="72280-118">작업 개체</span><span class="sxs-lookup"><span data-stu-id="72280-118">Operation object</span></span>

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

### <span data-ttu-id="72280-119">-이름</span><span class="sxs-lookup"><span data-stu-id="72280-119">-Name</span></span>
<span data-ttu-id="72280-120">인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72280-120">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="72280-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72280-121">-PassThru</span></span>
<span data-ttu-id="72280-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="72280-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="72280-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72280-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72280-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="72280-124">-VaultName</span></span>
<span data-ttu-id="72280-125">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="72280-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="72280-126">-확인</span><span class="sxs-lookup"><span data-stu-id="72280-126">-Confirm</span></span>
<span data-ttu-id="72280-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72280-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72280-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72280-128">-WhatIf</span></span>
<span data-ttu-id="72280-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72280-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72280-130">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72280-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72280-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72280-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72280-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72280-132">CommonParameters</span></span>
<span data-ttu-id="72280-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72280-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72280-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72280-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72280-135">입력</span><span class="sxs-lookup"><span data-stu-id="72280-135">INPUTS</span></span>

### <span data-ttu-id="72280-136">않아야</span><span class="sxs-lookup"><span data-stu-id="72280-136">None</span></span>
<span data-ttu-id="72280-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72280-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72280-138">출력</span><span class="sxs-lookup"><span data-stu-id="72280-138">OUTPUTS</span></span>

### <span data-ttu-id="72280-139">Microsoft. KeyVault. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="72280-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="72280-140">상속자</span><span class="sxs-lookup"><span data-stu-id="72280-140">NOTES</span></span>

## <span data-ttu-id="72280-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72280-141">RELATED LINKS</span></span>

[<span data-ttu-id="72280-142">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="72280-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="72280-143">중지-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="72280-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

