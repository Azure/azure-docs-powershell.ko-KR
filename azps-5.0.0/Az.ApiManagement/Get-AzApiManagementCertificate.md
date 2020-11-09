---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308471"
---
# <span data-ttu-id="35803-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="35803-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="35803-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35803-102">SYNOPSIS</span></span>
<span data-ttu-id="35803-103">서비스에서 백엔드를 사용 하 여 상호 인증 하도록 구성 된 API Management 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35803-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="35803-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35803-104">SYNTAX</span></span>

### <span data-ttu-id="35803-105">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="35803-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35803-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35803-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35803-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35803-107">DESCRIPTION</span></span>
<span data-ttu-id="35803-108">**AzApiManagementCertificate** cmdlet은 지정 하는 모든 Azure API Management 인증서 또는 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35803-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="35803-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35803-109">EXAMPLES</span></span>

### <span data-ttu-id="35803-110">예제 1: 모든 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="35803-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="35803-111">이 명령은 모든 API Management 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35803-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="35803-112">예제 2: 해당 ID로 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="35803-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="35803-113">이 명령은 지정 된 ID를 가진 API Management 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35803-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="35803-114">변수</span><span class="sxs-lookup"><span data-stu-id="35803-114">PARAMETERS</span></span>

### <span data-ttu-id="35803-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="35803-115">-CertificateId</span></span>
<span data-ttu-id="35803-116">가져올 인증서의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35803-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="35803-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="35803-117">-Context</span></span>
<span data-ttu-id="35803-118">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35803-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35803-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35803-119">-DefaultProfile</span></span>
<span data-ttu-id="35803-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35803-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35803-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35803-121">-ResourceId</span></span>
<span data-ttu-id="35803-122">인증서의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="35803-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="35803-123">지정 된 경우 식별자를 사용 하 여 인증서를 찾아 봅니다.</span><span class="sxs-lookup"><span data-stu-id="35803-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="35803-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="35803-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35803-125">-확인</span><span class="sxs-lookup"><span data-stu-id="35803-125">-Confirm</span></span>
<span data-ttu-id="35803-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35803-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35803-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35803-127">-WhatIf</span></span>
<span data-ttu-id="35803-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35803-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35803-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35803-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35803-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35803-130">CommonParameters</span></span>
<span data-ttu-id="35803-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35803-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35803-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="35803-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35803-133">입력</span><span class="sxs-lookup"><span data-stu-id="35803-133">INPUTS</span></span>

### <span data-ttu-id="35803-134">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="35803-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="35803-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35803-135">System.String</span></span>

## <span data-ttu-id="35803-136">출력</span><span class="sxs-lookup"><span data-stu-id="35803-136">OUTPUTS</span></span>

### <span data-ttu-id="35803-137">ApiManagement. ServiceManagement. \ PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="35803-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="35803-138">상속자</span><span class="sxs-lookup"><span data-stu-id="35803-138">NOTES</span></span>

## <span data-ttu-id="35803-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35803-139">RELATED LINKS</span></span>

[<span data-ttu-id="35803-140">새로운 AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="35803-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="35803-141">제거-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="35803-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="35803-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="35803-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


