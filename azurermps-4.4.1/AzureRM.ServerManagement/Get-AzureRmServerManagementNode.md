---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: ab49458426b7035a20e63ca62d86124d79291b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530689"
---
# <span data-ttu-id="11b7c-101">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="11b7c-101">Get-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="11b7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="11b7c-103">하나 이상의 서버 관리 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11b7c-103">Gets one or more Server Management nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11b7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11b7c-104">SYNTAX</span></span>

### <span data-ttu-id="11b7c-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="11b7c-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11b7c-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="11b7c-106">ByNode</span></span>
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11b7c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="11b7c-107">DESCRIPTION</span></span>
<span data-ttu-id="11b7c-108">**AzureRmServerManagementNode** cmdlet은 하나 이상의 Azure 서버 관리 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11b7c-108">The **Get-AzureRmServerManagementNode** cmdlet gets one or more Azure Server Management nodes.</span></span>

## <span data-ttu-id="11b7c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="11b7c-109">EXAMPLES</span></span>

## <span data-ttu-id="11b7c-110">변수</span><span class="sxs-lookup"><span data-stu-id="11b7c-110">PARAMETERS</span></span>

### <span data-ttu-id="11b7c-111">-노드</span><span class="sxs-lookup"><span data-stu-id="11b7c-111">-Node</span></span>
<span data-ttu-id="11b7c-112">*ResourceGroupName* 및 *NodeName* 매개 변수를 가져올 기존 노드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b7c-112">Specifies an existing node from which to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11b7c-113">-NodeName</span><span class="sxs-lookup"><span data-stu-id="11b7c-113">-NodeName</span></span>
<span data-ttu-id="11b7c-114">이 cmdlet이 가져오는 노드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b7c-114">Specifies the name of the node for which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11b7c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b7c-115">-ResourceGroupName</span></span>
<span data-ttu-id="11b7c-116">노드가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b7c-116">Specifies the name of the resource group in which the nodes belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11b7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b7c-117">-DefaultProfile</span></span>
<span data-ttu-id="11b7c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11b7c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11b7c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b7c-119">CommonParameters</span></span>
<span data-ttu-id="11b7c-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b7c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b7c-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b7c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b7c-122">입력</span><span class="sxs-lookup"><span data-stu-id="11b7c-122">INPUTS</span></span>

### <span data-ttu-id="11b7c-123">노드나</span><span class="sxs-lookup"><span data-stu-id="11b7c-123">Node</span></span>
<span data-ttu-id="11b7c-124">' Node ' 매개 변수는 파이프라인에서 ' Node ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b7c-124">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="11b7c-125">출력</span><span class="sxs-lookup"><span data-stu-id="11b7c-125">OUTPUTS</span></span>

### <span data-ttu-id="11b7c-126">Microsoft. ServerManagement. 모델 노드</span><span class="sxs-lookup"><span data-stu-id="11b7c-126">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="11b7c-127">상속자</span><span class="sxs-lookup"><span data-stu-id="11b7c-127">NOTES</span></span>

## <span data-ttu-id="11b7c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11b7c-128">RELATED LINKS</span></span>

[<span data-ttu-id="11b7c-129">새로운 AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="11b7c-129">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)

[<span data-ttu-id="11b7c-130">제거-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="11b7c-130">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


