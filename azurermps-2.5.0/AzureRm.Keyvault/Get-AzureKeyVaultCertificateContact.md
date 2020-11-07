---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: d6d2070afcb4a5b9b0b13af1fa54dc93621c5a97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881526"
---
# <span data-ttu-id="cd7e1-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cd7e1-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="cd7e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7e1-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7e1-103">키 자격 증명 모음에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd7e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd7e1-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd7e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cd7e1-105">DESCRIPTION</span></span>
<span data-ttu-id="cd7e1-106">**AzureKeyVaultCertificateContact** Cmdlet은 Azure key vault의 키 보관소에 대 한 인증서 알림에 대해 등록 된 연락처를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="cd7e1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cd7e1-107">EXAMPLES</span></span>

### <span data-ttu-id="cd7e1-108">예제 1: 모든 인증서 연락처 가져오기</span><span class="sxs-lookup"><span data-stu-id="cd7e1-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="cd7e1-109">이 명령은 Contoso 키 자격 증명 모음의 인증서 개체에 대 한 모든 연락처를 가져온 다음 $Contacts 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="cd7e1-110">변수</span><span class="sxs-lookup"><span data-stu-id="cd7e1-110">PARAMETERS</span></span>

### <span data-ttu-id="cd7e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7e1-111">-DefaultProfile</span></span>
<span data-ttu-id="cd7e1-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cd7e1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd7e1-113">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cd7e1-113">-VaultName</span></span>
<span data-ttu-id="cd7e1-114">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="cd7e1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7e1-115">CommonParameters</span></span>
<span data-ttu-id="cd7e1-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd7e1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7e1-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd7e1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7e1-118">입력</span><span class="sxs-lookup"><span data-stu-id="cd7e1-118">INPUTS</span></span>

## <span data-ttu-id="cd7e1-119">출력</span><span class="sxs-lookup"><span data-stu-id="cd7e1-119">OUTPUTS</span></span>

### <span data-ttu-id="cd7e1-120"><를 나열 합니다. KeyVault. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="cd7e1-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="cd7e1-121">상속자</span><span class="sxs-lookup"><span data-stu-id="cd7e1-121">NOTES</span></span>

## <span data-ttu-id="cd7e1-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd7e1-122">RELATED LINKS</span></span>

[<span data-ttu-id="cd7e1-123">추가-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cd7e1-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="cd7e1-124">제거-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cd7e1-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

