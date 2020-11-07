---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: b6825d23244664b475dbd28472dc30f33117a59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703287"
---
# <span data-ttu-id="21e21-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="21e21-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="21e21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21e21-102">SYNOPSIS</span></span>
<span data-ttu-id="21e21-103">서비스에서 백엔드를 사용 하 여 상호 인증 하도록 구성 된 API Management 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21e21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="21e21-104">SYNTAX</span></span>

### <span data-ttu-id="21e21-105">GetAllCertificates (기본값)</span><span class="sxs-lookup"><span data-stu-id="21e21-105">GetAllCertificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e21-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="21e21-106">GetByCertificateId</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21e21-107">설명은</span><span class="sxs-lookup"><span data-stu-id="21e21-107">DESCRIPTION</span></span>
<span data-ttu-id="21e21-108">**AzureRmApiManagementCertificate** cmdlet은 지정 하는 모든 Azure API Management 인증서 또는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="21e21-109">예제의</span><span class="sxs-lookup"><span data-stu-id="21e21-109">EXAMPLES</span></span>

### <span data-ttu-id="21e21-110">예제 1: 모든 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="21e21-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="21e21-111">이 명령은 모든 API Management 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="21e21-112">예제 2: 해당 ID로 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="21e21-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="21e21-113">이 명령은 지정 된 ID를 가진 API Management 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="21e21-114">변수</span><span class="sxs-lookup"><span data-stu-id="21e21-114">PARAMETERS</span></span>

### <span data-ttu-id="21e21-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="21e21-115">-CertificateId</span></span>
<span data-ttu-id="21e21-116">가져올 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByCertificateId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21e21-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="21e21-117">-Context</span></span>
<span data-ttu-id="21e21-118">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21e21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e21-119">-DefaultProfile</span></span>
<span data-ttu-id="21e21-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="21e21-121">-확인</span><span class="sxs-lookup"><span data-stu-id="21e21-121">-Confirm</span></span>
<span data-ttu-id="21e21-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21e21-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21e21-123">-WhatIf</span></span>
<span data-ttu-id="21e21-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21e21-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21e21-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e21-126">CommonParameters</span></span>
<span data-ttu-id="21e21-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e21-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e21-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e21-129">입력</span><span class="sxs-lookup"><span data-stu-id="21e21-129">INPUTS</span></span>

### <span data-ttu-id="21e21-130">않아야</span><span class="sxs-lookup"><span data-stu-id="21e21-130">None</span></span>
<span data-ttu-id="21e21-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="21e21-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21e21-132">출력</span><span class="sxs-lookup"><span data-stu-id="21e21-132">OUTPUTS</span></span>

### <span data-ttu-id="21e21-133">ApiManagement. ServiceManagement. \ PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="21e21-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="21e21-134">상속자</span><span class="sxs-lookup"><span data-stu-id="21e21-134">NOTES</span></span>

## <span data-ttu-id="21e21-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21e21-135">RELATED LINKS</span></span>

[<span data-ttu-id="21e21-136">새로운 AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="21e21-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="21e21-137">제거-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="21e21-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="21e21-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="21e21-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


