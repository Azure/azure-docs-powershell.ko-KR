---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 93efff5a9f317b7d44d071a4dd212d235df02223
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530673"
---
# <span data-ttu-id="81e54-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="81e54-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="81e54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81e54-102">SYNOPSIS</span></span>
<span data-ttu-id="81e54-103">서버 관리 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e54-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81e54-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81e54-104">SYNTAX</span></span>

### <span data-ttu-id="81e54-105">ByName</span><span class="sxs-lookup"><span data-stu-id="81e54-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81e54-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="81e54-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81e54-107">설명은</span><span class="sxs-lookup"><span data-stu-id="81e54-107">DESCRIPTION</span></span>
<span data-ttu-id="81e54-108">**AzureRmServerManagementNode** Cmdlet은 Azure 서버 관리 노드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e54-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="81e54-109">예제의</span><span class="sxs-lookup"><span data-stu-id="81e54-109">EXAMPLES</span></span>

## <span data-ttu-id="81e54-110">변수</span><span class="sxs-lookup"><span data-stu-id="81e54-110">PARAMETERS</span></span>

### <span data-ttu-id="81e54-111">-노드</span><span class="sxs-lookup"><span data-stu-id="81e54-111">-Node</span></span>
<span data-ttu-id="81e54-112">이 cmdlet이 제거할 노드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e54-112">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="81e54-113">이 매개 변수는 *ResourceGroupName* 및 *NodeName* 매개 변수 대신 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="81e54-113">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81e54-114">-NodeName</span><span class="sxs-lookup"><span data-stu-id="81e54-114">-NodeName</span></span>
<span data-ttu-id="81e54-115">이 cmdlet이 제거 되는 노드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e54-115">Specifies the name of the node for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81e54-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e54-116">-ResourceGroupName</span></span>
<span data-ttu-id="81e54-117">노드가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e54-117">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81e54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e54-118">-DefaultProfile</span></span>
<span data-ttu-id="81e54-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81e54-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81e54-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e54-120">CommonParameters</span></span>
<span data-ttu-id="81e54-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e54-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e54-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81e54-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e54-123">입력</span><span class="sxs-lookup"><span data-stu-id="81e54-123">INPUTS</span></span>

### <span data-ttu-id="81e54-124">노드나</span><span class="sxs-lookup"><span data-stu-id="81e54-124">Node</span></span>
<span data-ttu-id="81e54-125">' Node ' 매개 변수는 파이프라인에서 ' Node ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="81e54-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="81e54-126">출력</span><span class="sxs-lookup"><span data-stu-id="81e54-126">OUTPUTS</span></span>

## <span data-ttu-id="81e54-127">상속자</span><span class="sxs-lookup"><span data-stu-id="81e54-127">NOTES</span></span>

## <span data-ttu-id="81e54-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81e54-128">RELATED LINKS</span></span>

[<span data-ttu-id="81e54-129">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="81e54-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="81e54-130">새로운 AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="81e54-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


