---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 53bf195bf801b4746f0ea958949f1683c8ca3d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703544"
---
# <span data-ttu-id="37284-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="37284-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="37284-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37284-102">SYNOPSIS</span></span>
<span data-ttu-id="37284-103">서버 관리 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="37284-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37284-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37284-104">SYNTAX</span></span>

### <span data-ttu-id="37284-105">ByName</span><span class="sxs-lookup"><span data-stu-id="37284-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37284-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="37284-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37284-107">설명은</span><span class="sxs-lookup"><span data-stu-id="37284-107">DESCRIPTION</span></span>
<span data-ttu-id="37284-108">**AzureRmServerManagementGateway** Cmdlet은 Azure 서버 관리 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="37284-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="37284-109">예제의</span><span class="sxs-lookup"><span data-stu-id="37284-109">EXAMPLES</span></span>

## <span data-ttu-id="37284-110">변수</span><span class="sxs-lookup"><span data-stu-id="37284-110">PARAMETERS</span></span>

### <span data-ttu-id="37284-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37284-111">-DefaultProfile</span></span>
<span data-ttu-id="37284-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37284-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37284-113">-게이트웨이</span><span class="sxs-lookup"><span data-stu-id="37284-113">-Gateway</span></span>
<span data-ttu-id="37284-114">이 cmdlet이 제거 하는 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37284-114">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="37284-115">이 매개 변수는 *ResourceGroupName* 및 *이름* 매개 변수 대신 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37284-115">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37284-116">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="37284-116">-GatewayName</span></span>
<span data-ttu-id="37284-117">이 cmdlet이 제거 하는 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37284-117">Specifies the name of the gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37284-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37284-118">-ResourceGroupName</span></span>
<span data-ttu-id="37284-119">게이트웨이가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37284-119">Specifies the name of the resource group in that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37284-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37284-120">CommonParameters</span></span>
<span data-ttu-id="37284-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37284-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37284-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37284-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37284-123">입력</span><span class="sxs-lookup"><span data-stu-id="37284-123">INPUTS</span></span>

### <span data-ttu-id="37284-124">게이트웨이와</span><span class="sxs-lookup"><span data-stu-id="37284-124">Gateway</span></span>
<span data-ttu-id="37284-125">' Gateway ' 매개 변수는 파이프라인에서 ' Gateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37284-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="37284-126">출력</span><span class="sxs-lookup"><span data-stu-id="37284-126">OUTPUTS</span></span>

## <span data-ttu-id="37284-127">상속자</span><span class="sxs-lookup"><span data-stu-id="37284-127">NOTES</span></span>
* <span data-ttu-id="37284-128">이 cmdlet을 사용 하기 전에 게이트웨이에 있는 모든 노드를 제거 해야 합니다. 그렇지 않은 경우에는이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="37284-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="37284-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37284-129">RELATED LINKS</span></span>

[<span data-ttu-id="37284-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="37284-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="37284-131">새로운 AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="37284-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


