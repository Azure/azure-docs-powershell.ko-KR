---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: f73d53fc3031fc72be950547e5b9c2b93a9a0079
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702358"
---
# <span data-ttu-id="4abb1-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4abb1-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="4abb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4abb1-102">SYNOPSIS</span></span>
<span data-ttu-id="4abb1-103">서버 관리 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4abb1-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4abb1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4abb1-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4abb1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4abb1-105">DESCRIPTION</span></span>
<span data-ttu-id="4abb1-106">**AzureRmServerManagementGateway** Cmdlet은 Azure 서버 관리 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4abb1-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="4abb1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4abb1-107">EXAMPLES</span></span>

## <span data-ttu-id="4abb1-108">변수</span><span class="sxs-lookup"><span data-stu-id="4abb1-108">PARAMETERS</span></span>

### <span data-ttu-id="4abb1-109">-AutoUpgrade</span><span class="sxs-lookup"><span data-stu-id="4abb1-109">-AutoUpgrade</span></span>
<span data-ttu-id="4abb1-110">새 버전이 릴리스되면 게이트웨이가 자동으로 업그레이드 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4abb1-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abb1-111">-DefaultProfile</span></span>
<span data-ttu-id="4abb1-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4abb1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4abb1-113">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="4abb1-113">-GatewayName</span></span>
<span data-ttu-id="4abb1-114">이 cmdlet이 만드는 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4abb1-114">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-115">-위치</span><span class="sxs-lookup"><span data-stu-id="4abb1-115">-Location</span></span>
<span data-ttu-id="4abb1-116">게이트웨이를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4abb1-116">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4abb1-117">-ResourceGroupName</span></span>
<span data-ttu-id="4abb1-118">이 cmdlet이 게이트웨이를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4abb1-118">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-119">태그</span><span class="sxs-lookup"><span data-stu-id="4abb1-119">-Tag</span></span>
<span data-ttu-id="4abb1-120">게이트웨이와 연결 된 키/값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="4abb1-120">Key/value pairs associated with the gateway.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4abb1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abb1-121">CommonParameters</span></span>
<span data-ttu-id="4abb1-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4abb1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abb1-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4abb1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abb1-124">입력</span><span class="sxs-lookup"><span data-stu-id="4abb1-124">INPUTS</span></span>

### <span data-ttu-id="4abb1-125">않아야</span><span class="sxs-lookup"><span data-stu-id="4abb1-125">None</span></span>
<span data-ttu-id="4abb1-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4abb1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4abb1-127">출력</span><span class="sxs-lookup"><span data-stu-id="4abb1-127">OUTPUTS</span></span>

### <span data-ttu-id="4abb1-128">Microsoft. ServerManagement. 모델 게이트웨이</span><span class="sxs-lookup"><span data-stu-id="4abb1-128">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="4abb1-129">상속자</span><span class="sxs-lookup"><span data-stu-id="4abb1-129">NOTES</span></span>

## <span data-ttu-id="4abb1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4abb1-130">RELATED LINKS</span></span>

[<span data-ttu-id="4abb1-131">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4abb1-131">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="4abb1-132">제거-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4abb1-132">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


