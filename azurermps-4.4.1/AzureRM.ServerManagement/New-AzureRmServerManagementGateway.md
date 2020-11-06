---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9cb98b9671f43ddd7acbcc84e8473a12da00f405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530676"
---
# <span data-ttu-id="95ab8-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="95ab8-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="95ab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="95ab8-103">서버 관리 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95ab8-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95ab8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95ab8-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95ab8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="95ab8-106">**AzureRmServerManagementGateway** Cmdlet은 Azure 서버 관리 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="95ab8-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="95ab8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95ab8-107">EXAMPLES</span></span>

## <span data-ttu-id="95ab8-108">변수</span><span class="sxs-lookup"><span data-stu-id="95ab8-108">PARAMETERS</span></span>

### <span data-ttu-id="95ab8-109">-AutoUpgrade</span><span class="sxs-lookup"><span data-stu-id="95ab8-109">-AutoUpgrade</span></span>
<span data-ttu-id="95ab8-110">새 버전이 릴리스되면 게이트웨이가 자동으로 업그레이드 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="95ab8-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

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

### <span data-ttu-id="95ab8-111">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="95ab8-111">-GatewayName</span></span>
<span data-ttu-id="95ab8-112">이 cmdlet이 만드는 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ab8-112">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ab8-113">-위치</span><span class="sxs-lookup"><span data-stu-id="95ab8-113">-Location</span></span>
<span data-ttu-id="95ab8-114">게이트웨이를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ab8-114">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ab8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ab8-115">-ResourceGroupName</span></span>
<span data-ttu-id="95ab8-116">이 cmdlet이 게이트웨이를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ab8-116">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ab8-117">태그</span><span class="sxs-lookup"><span data-stu-id="95ab8-117">-Tags</span></span>
<span data-ttu-id="95ab8-118">태그를 키-값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ab8-118">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="95ab8-119">태그를 사용 하 여 다른 Azure 리소스에서 게이트웨이를 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95ab8-119">You can use tags to identify a Gateway from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ab8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ab8-120">-DefaultProfile</span></span>
<span data-ttu-id="95ab8-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95ab8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95ab8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ab8-122">CommonParameters</span></span>
<span data-ttu-id="95ab8-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95ab8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ab8-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ab8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ab8-125">입력</span><span class="sxs-lookup"><span data-stu-id="95ab8-125">INPUTS</span></span>

## <span data-ttu-id="95ab8-126">출력</span><span class="sxs-lookup"><span data-stu-id="95ab8-126">OUTPUTS</span></span>

### <span data-ttu-id="95ab8-127">Microsoft. ServerManagement. 모델 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="95ab8-127">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="95ab8-128">상속자</span><span class="sxs-lookup"><span data-stu-id="95ab8-128">NOTES</span></span>

## <span data-ttu-id="95ab8-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95ab8-129">RELATED LINKS</span></span>

[<span data-ttu-id="95ab8-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="95ab8-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="95ab8-131">제거-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="95ab8-131">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


