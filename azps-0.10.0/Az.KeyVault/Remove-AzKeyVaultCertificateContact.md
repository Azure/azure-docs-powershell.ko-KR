---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 0b92fcb3725d42ac7c2978600f7903d6bf7f6142
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875821"
---
# <span data-ttu-id="612c3-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="612c3-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="612c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="612c3-102">SYNOPSIS</span></span>
<span data-ttu-id="612c3-103">키 보관소의 인증서 알림에 대해 등록 된 대화 상대를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="612c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="612c3-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="612c3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="612c3-105">DESCRIPTION</span></span>
<span data-ttu-id="612c3-106">**AzKeyVaultCertificateContact** cmdlet은 키 보관소의 인증서 알림에 대해 등록 된 연락처를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-106">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="612c3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="612c3-107">EXAMPLES</span></span>

### <span data-ttu-id="612c3-108">예제 1: 인증서 연락처 제거</span><span class="sxs-lookup"><span data-stu-id="612c3-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="612c3-109">이 명령은 Patti을 Contoso01 키 보관소의 인증서 연락처로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="612c3-110">변수</span><span class="sxs-lookup"><span data-stu-id="612c3-110">PARAMETERS</span></span>

### <span data-ttu-id="612c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="612c3-111">-DefaultProfile</span></span>
<span data-ttu-id="612c3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="612c3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="612c3-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="612c3-113">-EmailAddress</span></span>
<span data-ttu-id="612c3-114">제거할 연락처의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-114">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="612c3-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="612c3-115">-PassThru</span></span>
<span data-ttu-id="612c3-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="612c3-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="612c3-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="612c3-118">-VaultName</span></span>
<span data-ttu-id="612c3-119">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="612c3-120">-확인</span><span class="sxs-lookup"><span data-stu-id="612c3-120">-Confirm</span></span>
<span data-ttu-id="612c3-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="612c3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="612c3-122">-WhatIf</span></span>
<span data-ttu-id="612c3-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="612c3-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="612c3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="612c3-125">CommonParameters</span></span>
<span data-ttu-id="612c3-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="612c3-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="612c3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="612c3-128">입력</span><span class="sxs-lookup"><span data-stu-id="612c3-128">INPUTS</span></span>

### <span data-ttu-id="612c3-129">않아야</span><span class="sxs-lookup"><span data-stu-id="612c3-129">None</span></span>
<span data-ttu-id="612c3-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="612c3-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="612c3-131">출력</span><span class="sxs-lookup"><span data-stu-id="612c3-131">OUTPUTS</span></span>

### <span data-ttu-id="612c3-132">KeyVaultCertificateContact의 ' 1 [Microsoft Azure.] 목록. List.</span><span class="sxs-lookup"><span data-stu-id="612c3-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="612c3-133">상속자</span><span class="sxs-lookup"><span data-stu-id="612c3-133">NOTES</span></span>

## <span data-ttu-id="612c3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="612c3-134">RELATED LINKS</span></span>

[<span data-ttu-id="612c3-135">추가-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="612c3-135">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="612c3-136">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="612c3-136">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

