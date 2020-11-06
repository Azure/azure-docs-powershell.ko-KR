---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 1fbf5a5541fe3e1360e696f9c06a26d6ea131dc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534952"
---
# <span data-ttu-id="7840d-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7840d-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="7840d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7840d-102">SYNOPSIS</span></span>
<span data-ttu-id="7840d-103">키 보관소의 인증서 알림에 대해 등록 된 대화 상대를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7840d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7840d-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7840d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7840d-105">DESCRIPTION</span></span>
<span data-ttu-id="7840d-106">**AzureKeyVaultCertificateContact** cmdlet은 키 보관소의 인증서 알림에 대해 등록 된 연락처를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="7840d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7840d-107">EXAMPLES</span></span>

### <span data-ttu-id="7840d-108">예제 1: 인증서 연락처 제거</span><span class="sxs-lookup"><span data-stu-id="7840d-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="7840d-109">이 명령은 Patti을 Contoso01 키 보관소의 인증서 연락처로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="7840d-110">변수</span><span class="sxs-lookup"><span data-stu-id="7840d-110">PARAMETERS</span></span>

### <span data-ttu-id="7840d-111">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="7840d-111">-EmailAddress</span></span>
<span data-ttu-id="7840d-112">제거할 연락처의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-112">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="7840d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7840d-113">-PassThru</span></span>
<span data-ttu-id="7840d-114">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7840d-115">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7840d-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7840d-116">-VaultName</span></span>
<span data-ttu-id="7840d-117">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-117">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7840d-118">-확인</span><span class="sxs-lookup"><span data-stu-id="7840d-118">-Confirm</span></span>
<span data-ttu-id="7840d-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7840d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7840d-120">-WhatIf</span></span>
<span data-ttu-id="7840d-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7840d-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7840d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7840d-123">-DefaultProfile</span></span>
<span data-ttu-id="7840d-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7840d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7840d-125">CommonParameters</span></span>
<span data-ttu-id="7840d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7840d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7840d-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7840d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7840d-128">입력</span><span class="sxs-lookup"><span data-stu-id="7840d-128">INPUTS</span></span>

## <span data-ttu-id="7840d-129">출력</span><span class="sxs-lookup"><span data-stu-id="7840d-129">OUTPUTS</span></span>

### <span data-ttu-id="7840d-130">KeyVaultCertificateContact의 ' 1 [Microsoft Azure.] 목록. List.</span><span class="sxs-lookup"><span data-stu-id="7840d-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="7840d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7840d-131">NOTES</span></span>

## <span data-ttu-id="7840d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7840d-132">RELATED LINKS</span></span>

[<span data-ttu-id="7840d-133">추가-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7840d-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="7840d-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7840d-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

