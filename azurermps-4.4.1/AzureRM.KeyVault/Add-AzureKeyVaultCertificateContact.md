---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: af66ad82d37c29d1dcd455cb3ccf7ae11676828c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536351"
---
# <span data-ttu-id="5c3ad-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5c3ad-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="5c3ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="5c3ad-103">인증서 알림에 대 한 대화 상대를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c3ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c3ad-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c3ad-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c3ad-105">DESCRIPTION</span></span>
<span data-ttu-id="5c3ad-106">**AzureKeyVaultCertificateContact** Cmdlet은 Azure key vault의 인증서 알림 용 키 보관소에 대 한 연락처를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="5c3ad-107">연락처가 만료, 인증서 갱신 등의 인증서와 같은 이벤트에 대 한 업데이트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="5c3ad-108">이러한 이벤트는 인증서 정책에 따라 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="5c3ad-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5c3ad-109">EXAMPLES</span></span>

### <span data-ttu-id="5c3ad-110">예제 1: 주요 자격 증명 모음 인증서 연락처 추가</span><span class="sxs-lookup"><span data-stu-id="5c3ad-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="5c3ad-111">이 명령은 Patti을 ContosoKV01 키 볼트에 대 한 인증서 연락처로 추가 하 고 **KeyVaultCertificateContact** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="5c3ad-112">변수</span><span class="sxs-lookup"><span data-stu-id="5c3ad-112">PARAMETERS</span></span>

### <span data-ttu-id="5c3ad-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5c3ad-113">-EmailAddress</span></span>
<span data-ttu-id="5c3ad-114">연락처의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-114">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c3ad-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c3ad-115">-PassThru</span></span>
<span data-ttu-id="5c3ad-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5c3ad-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c3ad-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5c3ad-118">-VaultName</span></span>
<span data-ttu-id="5c3ad-119">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-119">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="5c3ad-120">-확인</span><span class="sxs-lookup"><span data-stu-id="5c3ad-120">-Confirm</span></span>
<span data-ttu-id="5c3ad-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c3ad-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c3ad-122">-WhatIf</span></span>
<span data-ttu-id="5c3ad-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c3ad-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c3ad-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c3ad-125">-DefaultProfile</span></span>
<span data-ttu-id="5c3ad-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c3ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c3ad-127">CommonParameters</span></span>
<span data-ttu-id="5c3ad-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c3ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c3ad-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c3ad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c3ad-130">입력</span><span class="sxs-lookup"><span data-stu-id="5c3ad-130">INPUTS</span></span>

## <span data-ttu-id="5c3ad-131">출력</span><span class="sxs-lookup"><span data-stu-id="5c3ad-131">OUTPUTS</span></span>

### <span data-ttu-id="5c3ad-132"><를 나열 합니다. KeyVault. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="5c3ad-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="5c3ad-133">상속자</span><span class="sxs-lookup"><span data-stu-id="5c3ad-133">NOTES</span></span>

## <span data-ttu-id="5c3ad-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c3ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="5c3ad-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5c3ad-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="5c3ad-136">제거-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5c3ad-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

