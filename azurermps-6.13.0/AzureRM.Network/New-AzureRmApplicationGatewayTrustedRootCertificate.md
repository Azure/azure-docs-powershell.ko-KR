---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5f71f9a28eb1daae1bee070907675c87002241f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537583"
---
# <span data-ttu-id="0913f-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0913f-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="0913f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0913f-102">SYNOPSIS</span></span>
<span data-ttu-id="0913f-103">응용 프로그램 게이트웨이에 대해 신뢰할 수 있는 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0913f-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0913f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0913f-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0913f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0913f-105">DESCRIPTION</span></span>
<span data-ttu-id="0913f-106">**AzureRmApplicationGatewayTrustedRootCertificate** Cmdlet은 Azure application gateway에 대해 신뢰할 수 있는 루트 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0913f-106">The **New-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="0913f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0913f-107">EXAMPLES</span></span>

### <span data-ttu-id="0913f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0913f-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzureRmApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="0913f-109">이 명령은 "trc1" 이라는 신뢰할 수 있는 루트 인증서를 만들고 결과를 $trc 이름이 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0913f-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="0913f-110">변수</span><span class="sxs-lookup"><span data-stu-id="0913f-110">PARAMETERS</span></span>

### <span data-ttu-id="0913f-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0913f-111">-CertificateFile</span></span>
<span data-ttu-id="0913f-112">인증서 CER 파일 경로</span><span class="sxs-lookup"><span data-stu-id="0913f-112">Path of certificate CER file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0913f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0913f-113">-DefaultProfile</span></span>
<span data-ttu-id="0913f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0913f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0913f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0913f-115">-Name</span></span>
<span data-ttu-id="0913f-116">(이)가 게 된 루트 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0913f-116">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0913f-117">-확인</span><span class="sxs-lookup"><span data-stu-id="0913f-117">-Confirm</span></span>
<span data-ttu-id="0913f-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0913f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0913f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0913f-119">-WhatIf</span></span>
<span data-ttu-id="0913f-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0913f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0913f-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0913f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0913f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0913f-122">CommonParameters</span></span>
<span data-ttu-id="0913f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0913f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0913f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0913f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0913f-125">입력</span><span class="sxs-lookup"><span data-stu-id="0913f-125">INPUTS</span></span>

### <span data-ttu-id="0913f-126">않아야</span><span class="sxs-lookup"><span data-stu-id="0913f-126">None</span></span>

## <span data-ttu-id="0913f-127">출력</span><span class="sxs-lookup"><span data-stu-id="0913f-127">OUTPUTS</span></span>

### <span data-ttu-id="0913f-128">Microsoft. 네트워크. Psapplication게이트웨이를 위한 Rootcertificate</span><span class="sxs-lookup"><span data-stu-id="0913f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="0913f-129">상속자</span><span class="sxs-lookup"><span data-stu-id="0913f-129">NOTES</span></span>

## <span data-ttu-id="0913f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0913f-130">RELATED LINKS</span></span>
