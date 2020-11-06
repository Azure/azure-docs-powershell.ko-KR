---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: e607181b1f44508078f82b25e23e9d1fe53158db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527532"
---
# <span data-ttu-id="96cd3-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="96cd3-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="96cd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="96cd3-103">메모리 내 인증서 조직 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96cd3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96cd3-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96cd3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96cd3-105">DESCRIPTION</span></span>
<span data-ttu-id="96cd3-106">**AzureKeyVaultCertificateOrganizationDetails** cmdlet은 메모리 내 인증서 조직 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="96cd3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="96cd3-107">EXAMPLES</span></span>

### <span data-ttu-id="96cd3-108">예제 1: 조직 세부 정보 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="96cd3-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="96cd3-109">첫 번째 명령은 인증서 관리자 세부 정보 개체를 만든 다음 $AdminDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="96cd3-110">두 번째 명령은 인증서 조직 세부 정보 개체를 만든 다음 $OrgDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="96cd3-111">변수</span><span class="sxs-lookup"><span data-stu-id="96cd3-111">PARAMETERS</span></span>

### <span data-ttu-id="96cd3-112">-관리자 세부 정보</span><span class="sxs-lookup"><span data-stu-id="96cd3-112">-AdministratorDetails</span></span>
<span data-ttu-id="96cd3-113">인증서 조직 관리자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96cd3-114">-Id</span><span class="sxs-lookup"><span data-stu-id="96cd3-114">-Id</span></span>
<span data-ttu-id="96cd3-115">조직의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-115">Specifies the identifier for the organization.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96cd3-116">-확인</span><span class="sxs-lookup"><span data-stu-id="96cd3-116">-Confirm</span></span>
<span data-ttu-id="96cd3-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96cd3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96cd3-118">-WhatIf</span></span>
<span data-ttu-id="96cd3-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96cd3-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96cd3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96cd3-121">-DefaultProfile</span></span>
<span data-ttu-id="96cd3-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96cd3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cd3-123">CommonParameters</span></span>
<span data-ttu-id="96cd3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96cd3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cd3-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96cd3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cd3-126">입력</span><span class="sxs-lookup"><span data-stu-id="96cd3-126">INPUTS</span></span>

## <span data-ttu-id="96cd3-127">출력</span><span class="sxs-lookup"><span data-stu-id="96cd3-127">OUTPUTS</span></span>

### <span data-ttu-id="96cd3-128">Microsoft. KeyVault. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="96cd3-128">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="96cd3-129">상속자</span><span class="sxs-lookup"><span data-stu-id="96cd3-129">NOTES</span></span>

## <span data-ttu-id="96cd3-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96cd3-130">RELATED LINKS</span></span>

[<span data-ttu-id="96cd3-131">새로운 AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="96cd3-131">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

