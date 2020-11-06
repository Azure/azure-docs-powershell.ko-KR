---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 96f793c763a3e9a710c7e401c29880ccc0136b38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535979"
---
# <span data-ttu-id="cbb66-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cbb66-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="cbb66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbb66-102">SYNOPSIS</span></span>
<span data-ttu-id="cbb66-103">인증서 알림에 대 한 대화 상대를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbb66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cbb66-104">SYNTAX</span></span>

### <span data-ttu-id="cbb66-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cbb66-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbb66-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="cbb66-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbb66-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cbb66-107">DESCRIPTION</span></span>
<span data-ttu-id="cbb66-108">**AzureKeyVaultCertificateContact** Cmdlet은 Azure key vault의 인증서 알림 용 키 보관소에 대 한 연락처를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-108">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="cbb66-109">연락처가 만료, 인증서 갱신 등의 인증서와 같은 이벤트에 대 한 업데이트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-109">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="cbb66-110">이러한 이벤트는 인증서 정책에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-110">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="cbb66-111">예제의</span><span class="sxs-lookup"><span data-stu-id="cbb66-111">EXAMPLES</span></span>

### <span data-ttu-id="cbb66-112">예제 1: 주요 자격 증명 모음 인증서 연락처 추가</span><span class="sxs-lookup"><span data-stu-id="cbb66-112">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="cbb66-113">이 명령은 Patti을 ContosoKV01 키 볼트에 대 한 인증서 연락처로 추가 하 고 **KeyVaultCertificateContact** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-113">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="cbb66-114">변수</span><span class="sxs-lookup"><span data-stu-id="cbb66-114">PARAMETERS</span></span>

### <span data-ttu-id="cbb66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbb66-115">-DefaultProfile</span></span>
<span data-ttu-id="cbb66-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cbb66-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbb66-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="cbb66-117">-EmailAddress</span></span>
<span data-ttu-id="cbb66-118">연락처의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-118">Specifies the email address of the contact.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbb66-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbb66-119">-InputObject</span></span>
<span data-ttu-id="cbb66-120">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="cbb66-120">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbb66-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbb66-121">-PassThru</span></span>
<span data-ttu-id="cbb66-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cbb66-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cbb66-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cbb66-124">-VaultName</span></span>
<span data-ttu-id="cbb66-125">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-125">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbb66-126">-확인</span><span class="sxs-lookup"><span data-stu-id="cbb66-126">-Confirm</span></span>
<span data-ttu-id="cbb66-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbb66-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbb66-128">-WhatIf</span></span>
<span data-ttu-id="cbb66-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbb66-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbb66-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbb66-131">CommonParameters</span></span>
<span data-ttu-id="cbb66-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbb66-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbb66-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbb66-134">입력</span><span class="sxs-lookup"><span data-stu-id="cbb66-134">INPUTS</span></span>

### <span data-ttu-id="cbb66-135">않아야</span><span class="sxs-lookup"><span data-stu-id="cbb66-135">None</span></span>
<span data-ttu-id="cbb66-136">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbb66-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cbb66-137">출력</span><span class="sxs-lookup"><span data-stu-id="cbb66-137">OUTPUTS</span></span>

### <span data-ttu-id="cbb66-138"><를 나열 합니다. KeyVault. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="cbb66-138">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="cbb66-139">상속자</span><span class="sxs-lookup"><span data-stu-id="cbb66-139">NOTES</span></span>

## <span data-ttu-id="cbb66-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbb66-140">RELATED LINKS</span></span>

[<span data-ttu-id="cbb66-141">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cbb66-141">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="cbb66-142">제거-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cbb66-142">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

