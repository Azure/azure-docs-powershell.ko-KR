---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8942D757-B204-49CE-BCDE-68C3722913B3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
ms.openlocfilehash: e32f9268309562b45e13df164631e18d28cceb0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528821"
---
# <span data-ttu-id="1e6a7-101">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="1e6a7-101">Get-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="1e6a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6a7-103">서버 관리 세션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-103">Gets a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e6a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e6a7-104">SYNTAX</span></span>

### <span data-ttu-id="1e6a7-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="1e6a7-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e6a7-106">BySession</span><span class="sxs-lookup"><span data-stu-id="1e6a7-106">BySession</span></span>
```
Get-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e6a7-107">ByNode</span><span class="sxs-lookup"><span data-stu-id="1e6a7-107">ByNode</span></span>
```
Get-AzureRmServerManagementSession [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e6a7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1e6a7-108">DESCRIPTION</span></span>
<span data-ttu-id="1e6a7-109">**AzureRmServerManagementSession** cmdlet은 단일 Azure 서버 관리 세션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-109">The **Get-AzureRmServerManagementSession** cmdlet gets a single Azure Server Management session.</span></span>

## <span data-ttu-id="1e6a7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1e6a7-110">EXAMPLES</span></span>

## <span data-ttu-id="1e6a7-111">변수</span><span class="sxs-lookup"><span data-stu-id="1e6a7-111">PARAMETERS</span></span>

### <span data-ttu-id="1e6a7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6a7-112">-DefaultProfile</span></span>
<span data-ttu-id="1e6a7-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e6a7-114">-노드</span><span class="sxs-lookup"><span data-stu-id="1e6a7-114">-Node</span></span>
<span data-ttu-id="1e6a7-115">*ResourceGroupName* 및 *NodeName* 매개 변수를 가져오는 데 사용 되는 기존 **Node** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-115">Specifies an existing **Node** object that is used to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>
<span data-ttu-id="1e6a7-116">또한 *세션 이름* 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-116">You must also specify a value for the *SessionName* parameter.</span></span>

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6a7-117">-NodeName</span><span class="sxs-lookup"><span data-stu-id="1e6a7-117">-NodeName</span></span>
<span data-ttu-id="1e6a7-118">세션이 있는 노드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-118">Specifies the name of the node where the session is located.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e6a7-120">이 cmdlet이 세션 검색을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-120">Specifies the name of the resource group for which this cmdlet gets the retrieve the session.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6a7-121">-세션</span><span class="sxs-lookup"><span data-stu-id="1e6a7-121">-Session</span></span>
<span data-ttu-id="1e6a7-122">*ResourceGroupName* , *NodeName* 및 *세션 이름* 매개 변수를 가져오는 데 사용 되는 기존 **세션** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-122">Specifies an existing **Session** object that is used to get the *ResourceGroupName* , the *NodeName* , and the *SessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e6a7-123">-세션 이름</span><span class="sxs-lookup"><span data-stu-id="1e6a7-123">-SessionName</span></span>
<span data-ttu-id="1e6a7-124">이 cmdlet이 가져오는 세션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-124">Specifies the name of the session in which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySession
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6a7-125">CommonParameters</span></span>
<span data-ttu-id="1e6a7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6a7-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e6a7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6a7-128">입력</span><span class="sxs-lookup"><span data-stu-id="1e6a7-128">INPUTS</span></span>

### <span data-ttu-id="1e6a7-129">노드나</span><span class="sxs-lookup"><span data-stu-id="1e6a7-129">Node</span></span>
<span data-ttu-id="1e6a7-130">' Node ' 매개 변수는 파이프라인에서 ' Node ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-130">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

### <span data-ttu-id="1e6a7-131">세션만</span><span class="sxs-lookup"><span data-stu-id="1e6a7-131">Session</span></span>
<span data-ttu-id="1e6a7-132">' Session ' 매개 변수는 파이프라인에서 ' Session ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e6a7-132">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="1e6a7-133">출력</span><span class="sxs-lookup"><span data-stu-id="1e6a7-133">OUTPUTS</span></span>

### <span data-ttu-id="1e6a7-134">Microsoft. ServerManagement. Model. 세션</span><span class="sxs-lookup"><span data-stu-id="1e6a7-134">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="1e6a7-135">상속자</span><span class="sxs-lookup"><span data-stu-id="1e6a7-135">NOTES</span></span>

## <span data-ttu-id="1e6a7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e6a7-136">RELATED LINKS</span></span>

[<span data-ttu-id="1e6a7-137">Azure 서버 관리 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1e6a7-137">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


