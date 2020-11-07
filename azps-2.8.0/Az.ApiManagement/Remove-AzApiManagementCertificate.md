---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: fc22515fc1d1fc4c3975ee315ec9f7bf611e67c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697986"
---
# <span data-ttu-id="c17ce-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c17ce-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="c17ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c17ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c17ce-103">API Management 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="c17ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c17ce-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c17ce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c17ce-105">DESCRIPTION</span></span>
<span data-ttu-id="c17ce-106">**AzApiManagementCertificate** Cmdlet은 Azure API Management 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="c17ce-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c17ce-107">EXAMPLES</span></span>

### <span data-ttu-id="c17ce-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="c17ce-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="c17ce-109">이 명령은 지정 된 API Management 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="c17ce-110">*Force* 매개 변수는 지정 되어 있으므로 확인이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="c17ce-111">변수</span><span class="sxs-lookup"><span data-stu-id="c17ce-111">PARAMETERS</span></span>

### <span data-ttu-id="c17ce-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="c17ce-112">-CertificateId</span></span>
<span data-ttu-id="c17ce-113">제거할 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="c17ce-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="c17ce-114">-Context</span></span>
<span data-ttu-id="c17ce-115">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c17ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c17ce-116">-DefaultProfile</span></span>
<span data-ttu-id="c17ce-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c17ce-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c17ce-118">-PassThru</span></span>
<span data-ttu-id="c17ce-119">passthru</span><span class="sxs-lookup"><span data-stu-id="c17ce-119">passthru</span></span>

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

### <span data-ttu-id="c17ce-120">-확인</span><span class="sxs-lookup"><span data-stu-id="c17ce-120">-Confirm</span></span>
<span data-ttu-id="c17ce-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c17ce-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c17ce-122">-WhatIf</span></span>
<span data-ttu-id="c17ce-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c17ce-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c17ce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17ce-125">CommonParameters</span></span>
<span data-ttu-id="c17ce-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c17ce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17ce-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c17ce-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17ce-128">입력</span><span class="sxs-lookup"><span data-stu-id="c17ce-128">INPUTS</span></span>

### <span data-ttu-id="c17ce-129">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c17ce-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c17ce-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c17ce-130">System.String</span></span>

### <span data-ttu-id="c17ce-131">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c17ce-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c17ce-132">출력</span><span class="sxs-lookup"><span data-stu-id="c17ce-132">OUTPUTS</span></span>

### <span data-ttu-id="c17ce-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c17ce-133">System.Boolean</span></span>

## <span data-ttu-id="c17ce-134">상속자</span><span class="sxs-lookup"><span data-stu-id="c17ce-134">NOTES</span></span>

## <span data-ttu-id="c17ce-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c17ce-135">RELATED LINKS</span></span>

[<span data-ttu-id="c17ce-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c17ce-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="c17ce-137">새로운 AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c17ce-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="c17ce-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c17ce-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)

