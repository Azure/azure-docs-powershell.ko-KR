---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
ms.openlocfilehash: 50da8cae0af437ee86fd7462b285b812368b2508
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882226"
---
# <span data-ttu-id="7ce76-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="7ce76-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="7ce76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ce76-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce76-103">메모리 내 인증서 관리자 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ce76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ce76-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ce76-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7ce76-105">DESCRIPTION</span></span>
<span data-ttu-id="7ce76-106">**AzureKeyVaultCertificateAdministratorDetails** cmdlet은 메모리 내 인증서 관리자 세부 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="7ce76-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7ce76-107">EXAMPLES</span></span>

### <span data-ttu-id="7ce76-108">예제 1: 인증서 관리자 세부 정보 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="7ce76-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="7ce76-109">이 명령은 메모리 내 인증서 관리자 세부 정보 개체를 만든 다음이를 $AdminDetails 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="7ce76-110">변수</span><span class="sxs-lookup"><span data-stu-id="7ce76-110">PARAMETERS</span></span>

### <span data-ttu-id="7ce76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce76-111">-DefaultProfile</span></span>
<span data-ttu-id="7ce76-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7ce76-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ce76-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="7ce76-113">-EmailAddress</span></span>
<span data-ttu-id="7ce76-114">인증서 관리자의 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-114">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ce76-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="7ce76-115">-FirstName</span></span>
<span data-ttu-id="7ce76-116">인증서 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-116">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ce76-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="7ce76-117">-LastName</span></span>
<span data-ttu-id="7ce76-118">인증서 관리자의 성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-118">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ce76-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="7ce76-119">-PhoneNumber</span></span>
<span data-ttu-id="7ce76-120">인증서 관리자의 전화 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-120">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ce76-121">-확인</span><span class="sxs-lookup"><span data-stu-id="7ce76-121">-Confirm</span></span>
<span data-ttu-id="7ce76-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ce76-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ce76-123">-WhatIf</span></span>
<span data-ttu-id="7ce76-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ce76-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ce76-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce76-126">CommonParameters</span></span>
<span data-ttu-id="7ce76-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ce76-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce76-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ce76-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce76-129">입력</span><span class="sxs-lookup"><span data-stu-id="7ce76-129">INPUTS</span></span>

## <span data-ttu-id="7ce76-130">출력</span><span class="sxs-lookup"><span data-stu-id="7ce76-130">OUTPUTS</span></span>

### <span data-ttu-id="7ce76-131">Microsoft. KeyVault. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="7ce76-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="7ce76-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7ce76-132">NOTES</span></span>

## <span data-ttu-id="7ce76-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ce76-133">RELATED LINKS</span></span>

[<span data-ttu-id="7ce76-134">새로운 AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="7ce76-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)
