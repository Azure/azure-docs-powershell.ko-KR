---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 5844bbfd59e38691a28720d5cab4e73e334af88d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702284"
---
# <span data-ttu-id="01e88-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="01e88-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="01e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01e88-102">SYNOPSIS</span></span>
<span data-ttu-id="01e88-103">API Management 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01e88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01e88-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e88-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01e88-105">DESCRIPTION</span></span>
<span data-ttu-id="01e88-106">**AzureRmApiManagementCertificate** Cmdlet은 Azure API Management 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="01e88-107">예제의</span><span class="sxs-lookup"><span data-stu-id="01e88-107">EXAMPLES</span></span>

### <span data-ttu-id="01e88-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="01e88-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="01e88-109">이 명령은 지정 된 API Management 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="01e88-110">*Force* 매개 변수는 지정 되어 있으므로 확인이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="01e88-111">변수</span><span class="sxs-lookup"><span data-stu-id="01e88-111">PARAMETERS</span></span>

### <span data-ttu-id="01e88-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="01e88-112">-CertificateId</span></span>
<span data-ttu-id="01e88-113">제거할 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-113">Specifies the ID of the certificate to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e88-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="01e88-114">-Context</span></span>
<span data-ttu-id="01e88-115">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="01e88-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01e88-116">-PassThru</span></span>
<span data-ttu-id="01e88-117">passthru</span><span class="sxs-lookup"><span data-stu-id="01e88-117">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e88-118">-확인</span><span class="sxs-lookup"><span data-stu-id="01e88-118">-Confirm</span></span>
<span data-ttu-id="01e88-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e88-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e88-120">-WhatIf</span></span>
<span data-ttu-id="01e88-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e88-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e88-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e88-123">-DefaultProfile</span></span>
<span data-ttu-id="01e88-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01e88-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e88-125">CommonParameters</span></span>
<span data-ttu-id="01e88-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e88-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e88-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e88-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e88-128">입력</span><span class="sxs-lookup"><span data-stu-id="01e88-128">INPUTS</span></span>

## <span data-ttu-id="01e88-129">출력</span><span class="sxs-lookup"><span data-stu-id="01e88-129">OUTPUTS</span></span>

### <span data-ttu-id="01e88-130">나타내는</span><span class="sxs-lookup"><span data-stu-id="01e88-130">Boolean</span></span>

## <span data-ttu-id="01e88-131">상속자</span><span class="sxs-lookup"><span data-stu-id="01e88-131">NOTES</span></span>

## <span data-ttu-id="01e88-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01e88-132">RELATED LINKS</span></span>

[<span data-ttu-id="01e88-133">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="01e88-133">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="01e88-134">새로운 AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="01e88-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="01e88-135">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="01e88-135">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


