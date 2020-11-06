---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 167137cbb231bbd5093b118a22d33e2102159c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531298"
---
# <span data-ttu-id="39124-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="39124-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="39124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39124-102">SYNOPSIS</span></span>
<span data-ttu-id="39124-103">API Management 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39124-103">Gets API Management certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39124-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39124-104">SYNTAX</span></span>

### <span data-ttu-id="39124-105">모든 인증서 받기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="39124-105">Get all certificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39124-106">ID 별 인증서 받기</span><span class="sxs-lookup"><span data-stu-id="39124-106">Get certificate by ID</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39124-107">설명은</span><span class="sxs-lookup"><span data-stu-id="39124-107">DESCRIPTION</span></span>
<span data-ttu-id="39124-108">**AzureRmApiManagementCertificate** cmdlet은 지정 하는 모든 Azure API Management 인증서 또는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39124-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="39124-109">예제의</span><span class="sxs-lookup"><span data-stu-id="39124-109">EXAMPLES</span></span>

### <span data-ttu-id="39124-110">예제 1: 모든 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="39124-110">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="39124-111">이 명령은 모든 API Management 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39124-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="39124-112">예제 2: 해당 ID로 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="39124-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="39124-113">이 명령은 지정 된 ID를 가진 API Management 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39124-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="39124-114">변수</span><span class="sxs-lookup"><span data-stu-id="39124-114">PARAMETERS</span></span>

### <span data-ttu-id="39124-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="39124-115">-CertificateId</span></span>
<span data-ttu-id="39124-116">가져올 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39124-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get certificate by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39124-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="39124-117">-Context</span></span>
<span data-ttu-id="39124-118">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39124-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39124-119">-확인</span><span class="sxs-lookup"><span data-stu-id="39124-119">-Confirm</span></span>
<span data-ttu-id="39124-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39124-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39124-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39124-121">-WhatIf</span></span>
<span data-ttu-id="39124-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="39124-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39124-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39124-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39124-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39124-124">-DefaultProfile</span></span>
<span data-ttu-id="39124-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39124-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39124-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39124-126">CommonParameters</span></span>
<span data-ttu-id="39124-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39124-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39124-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39124-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39124-129">입력</span><span class="sxs-lookup"><span data-stu-id="39124-129">INPUTS</span></span>

## <span data-ttu-id="39124-130">출력</span><span class="sxs-lookup"><span data-stu-id="39124-130">OUTPUTS</span></span>

### <span data-ttu-id="39124-131">ApiManagement. ServiceManagement. \ PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="39124-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="39124-132">상속자</span><span class="sxs-lookup"><span data-stu-id="39124-132">NOTES</span></span>

## <span data-ttu-id="39124-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39124-133">RELATED LINKS</span></span>

[<span data-ttu-id="39124-134">새로운 AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="39124-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="39124-135">제거-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="39124-135">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="39124-136">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="39124-136">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


