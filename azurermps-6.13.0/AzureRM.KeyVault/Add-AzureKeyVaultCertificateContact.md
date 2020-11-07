---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c56dad380d1e5a43b3f4dafdc0e0e964e6264ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536644"
---
# <span data-ttu-id="e8ac2-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e8ac2-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e8ac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ac2-103">인증서 알림에 대 한 대화 상대를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8ac2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8ac2-104">SYNTAX</span></span>

### <span data-ttu-id="e8ac2-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e8ac2-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ac2-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e8ac2-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ac2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8ac2-107">ByResourceId</span></span>
```
Add-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ac2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e8ac2-108">DESCRIPTION</span></span>
<span data-ttu-id="e8ac2-109">**AzureKeyVaultCertificateContact** Cmdlet은 Azure key vault의 인증서 알림 용 키 보관소에 대 한 연락처를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-109">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="e8ac2-110">연락처가 만료, 인증서 갱신 등의 인증서와 같은 이벤트에 대 한 업데이트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="e8ac2-111">이러한 이벤트는 인증서 정책에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="e8ac2-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e8ac2-112">EXAMPLES</span></span>

### <span data-ttu-id="e8ac2-113">예제 1: 주요 자격 증명 모음 인증서 연락처 추가</span><span class="sxs-lookup"><span data-stu-id="e8ac2-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="e8ac2-114">이 명령은 Patti을 ContosoKV01 키 보관소에 대 한 인증서 연락처로 추가 하 고 "ContosoKV01" 볼트에 대 한 연락처 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="e8ac2-115">변수</span><span class="sxs-lookup"><span data-stu-id="e8ac2-115">PARAMETERS</span></span>

### <span data-ttu-id="e8ac2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ac2-116">-DefaultProfile</span></span>
<span data-ttu-id="e8ac2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e8ac2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8ac2-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e8ac2-118">-EmailAddress</span></span>
<span data-ttu-id="e8ac2-119">연락처의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8ac2-120">-InputObject</span></span>
<span data-ttu-id="e8ac2-121">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8ac2-122">-PassThru</span></span>
<span data-ttu-id="e8ac2-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e8ac2-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8ac2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8ac2-125">-ResourceId</span></span>
<span data-ttu-id="e8ac2-126">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-126">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac2-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e8ac2-127">-VaultName</span></span>
<span data-ttu-id="e8ac2-128">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ac2-129">-확인</span><span class="sxs-lookup"><span data-stu-id="e8ac2-129">-Confirm</span></span>
<span data-ttu-id="e8ac2-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ac2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ac2-131">-WhatIf</span></span>
<span data-ttu-id="e8ac2-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ac2-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ac2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ac2-134">CommonParameters</span></span>
<span data-ttu-id="e8ac2-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8ac2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ac2-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ac2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ac2-137">입력</span><span class="sxs-lookup"><span data-stu-id="e8ac2-137">INPUTS</span></span>

### <span data-ttu-id="e8ac2-138">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e8ac2-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="e8ac2-139">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8ac2-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e8ac2-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e8ac2-140">System.String</span></span>

## <span data-ttu-id="e8ac2-141">출력</span><span class="sxs-lookup"><span data-stu-id="e8ac2-141">OUTPUTS</span></span>

### <span data-ttu-id="e8ac2-142">Microsoft. KeyVault. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e8ac2-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e8ac2-143">상속자</span><span class="sxs-lookup"><span data-stu-id="e8ac2-143">NOTES</span></span>

## <span data-ttu-id="e8ac2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8ac2-144">RELATED LINKS</span></span>

[<span data-ttu-id="e8ac2-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e8ac2-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="e8ac2-146">제거-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e8ac2-146">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)
