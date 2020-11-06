---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: 498be36141d1a44d33cdcb351b92d5b6908071c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524924"
---
# <span data-ttu-id="c02ef-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="c02ef-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="c02ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c02ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c02ef-103">서버 관리 노드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c02ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c02ef-104">SYNTAX</span></span>

### <span data-ttu-id="c02ef-105">ByName</span><span class="sxs-lookup"><span data-stu-id="c02ef-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c02ef-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c02ef-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c02ef-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c02ef-107">DESCRIPTION</span></span>
<span data-ttu-id="c02ef-108">**AzureRmServerManagementNode** Cmdlet은 Azure 서버 관리 노드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="c02ef-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c02ef-109">EXAMPLES</span></span>

## <span data-ttu-id="c02ef-110">변수</span><span class="sxs-lookup"><span data-stu-id="c02ef-110">PARAMETERS</span></span>

### <span data-ttu-id="c02ef-111">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="c02ef-111">-ComputerName</span></span>
<span data-ttu-id="c02ef-112">관리 되는 컴퓨터의 컴퓨터 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-112">Specifies the computer name of the computer that is being managed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02ef-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="c02ef-113">-Credential</span></span>
<span data-ttu-id="c02ef-114">서버 관리 노드에 대 한 연결에 대 한 **PSCredential** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="c02ef-115">자격 증명 개체를 가져오려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="c02ef-116">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="c02ef-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02ef-117">-DefaultProfile</span></span>
<span data-ttu-id="c02ef-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c02ef-119">-게이트웨이</span><span class="sxs-lookup"><span data-stu-id="c02ef-119">-Gateway</span></span>
<span data-ttu-id="c02ef-120">노드를 관리 하는 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-120">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="c02ef-121">이 매개 변수는 *ResourceGroupName* , *게이트웨이 이름* 및 *위치* 매개 변수 대신 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-121">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

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

### <span data-ttu-id="c02ef-122">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="c02ef-122">-GatewayName</span></span>
<span data-ttu-id="c02ef-123">노드에 액세스 하는 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-123">Specifies the name of the gateway that accesses the node.</span></span>

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

### <span data-ttu-id="c02ef-124">-위치</span><span class="sxs-lookup"><span data-stu-id="c02ef-124">-Location</span></span>
<span data-ttu-id="c02ef-125">이 cmdlet이 노드를 만드는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-125">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02ef-126">-NodeName</span><span class="sxs-lookup"><span data-stu-id="c02ef-126">-NodeName</span></span>
<span data-ttu-id="c02ef-127">노드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-127">Specifies the name of the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02ef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c02ef-128">-ResourceGroupName</span></span>
<span data-ttu-id="c02ef-129">이 cmdlet이 노드를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-129">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="c02ef-130">태그</span><span class="sxs-lookup"><span data-stu-id="c02ef-130">-Tag</span></span>
<span data-ttu-id="c02ef-131">개체와 연결 된 키/값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-131">Key/value pairs associated with the object.</span></span>

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

### <span data-ttu-id="c02ef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02ef-132">CommonParameters</span></span>
<span data-ttu-id="c02ef-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02ef-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c02ef-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02ef-135">입력</span><span class="sxs-lookup"><span data-stu-id="c02ef-135">INPUTS</span></span>

### <span data-ttu-id="c02ef-136">게이트웨이와</span><span class="sxs-lookup"><span data-stu-id="c02ef-136">Gateway</span></span>
<span data-ttu-id="c02ef-137">' Gateway ' 매개 변수는 파이프라인에서 ' Gateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="c02ef-138">출력</span><span class="sxs-lookup"><span data-stu-id="c02ef-138">OUTPUTS</span></span>

### <span data-ttu-id="c02ef-139">Microsoft. ServerManagement. 모델 노드</span><span class="sxs-lookup"><span data-stu-id="c02ef-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="c02ef-140">상속자</span><span class="sxs-lookup"><span data-stu-id="c02ef-140">NOTES</span></span>

## <span data-ttu-id="c02ef-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c02ef-141">RELATED LINKS</span></span>

[<span data-ttu-id="c02ef-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="c02ef-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="c02ef-143">제거-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="c02ef-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


