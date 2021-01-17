---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: ab1623addbb415b1aa2f6a104904629d94b518d6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361418"
---
# <span data-ttu-id="00fbd-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="00fbd-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="00fbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="00fbd-103">API Management 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="00fbd-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="00fbd-104">구문</span><span class="sxs-lookup"><span data-stu-id="00fbd-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00fbd-105">설명</span><span class="sxs-lookup"><span data-stu-id="00fbd-105">DESCRIPTION</span></span>
<span data-ttu-id="00fbd-106">**Remove-AzApiManagementCertificate** cmdlet은 Azure API Management 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="00fbd-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="00fbd-107">예제</span><span class="sxs-lookup"><span data-stu-id="00fbd-107">EXAMPLES</span></span>

### <span data-ttu-id="00fbd-108">예제 1: 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="00fbd-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="00fbd-109">이 명령은 지정된 API Management 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="00fbd-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="00fbd-110">Force 매개 *변수가* 지정되어 있기 때문에 확인이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00fbd-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="00fbd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00fbd-111">PARAMETERS</span></span>

### <span data-ttu-id="00fbd-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="00fbd-112">-CertificateId</span></span>
<span data-ttu-id="00fbd-113">제거할 인증서의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00fbd-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="00fbd-114">-Context</span><span class="sxs-lookup"><span data-stu-id="00fbd-114">-Context</span></span>
<span data-ttu-id="00fbd-115">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="00fbd-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="00fbd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fbd-116">-DefaultProfile</span></span>
<span data-ttu-id="00fbd-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00fbd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00fbd-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00fbd-118">-PassThru</span></span>
<span data-ttu-id="00fbd-119">passthru</span><span class="sxs-lookup"><span data-stu-id="00fbd-119">passthru</span></span>

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

### <span data-ttu-id="00fbd-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00fbd-120">-Confirm</span></span>
<span data-ttu-id="00fbd-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="00fbd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00fbd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00fbd-122">-WhatIf</span></span>
<span data-ttu-id="00fbd-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="00fbd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00fbd-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00fbd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00fbd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fbd-125">CommonParameters</span></span>
<span data-ttu-id="00fbd-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00fbd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fbd-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00fbd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fbd-128">입력</span><span class="sxs-lookup"><span data-stu-id="00fbd-128">INPUTS</span></span>

### <span data-ttu-id="00fbd-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="00fbd-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="00fbd-130">System.String</span><span class="sxs-lookup"><span data-stu-id="00fbd-130">System.String</span></span>

### <span data-ttu-id="00fbd-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="00fbd-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="00fbd-132">출력</span><span class="sxs-lookup"><span data-stu-id="00fbd-132">OUTPUTS</span></span>

### <span data-ttu-id="00fbd-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00fbd-133">System.Boolean</span></span>

## <span data-ttu-id="00fbd-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00fbd-134">NOTES</span></span>

## <span data-ttu-id="00fbd-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00fbd-135">RELATED LINKS</span></span>

[<span data-ttu-id="00fbd-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="00fbd-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="00fbd-137">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="00fbd-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="00fbd-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="00fbd-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


