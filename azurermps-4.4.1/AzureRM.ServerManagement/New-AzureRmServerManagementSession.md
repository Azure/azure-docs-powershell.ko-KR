---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 0ae3e221ee39a00381f009f45a9a2f508a552b6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529158"
---
# <span data-ttu-id="8a56b-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="8a56b-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="8a56b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a56b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a56b-103">서버 관리 세션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a56b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a56b-104">SYNTAX</span></span>

### <span data-ttu-id="8a56b-105">ByName</span><span class="sxs-lookup"><span data-stu-id="8a56b-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a56b-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="8a56b-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a56b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8a56b-107">DESCRIPTION</span></span>
<span data-ttu-id="8a56b-108">**AzureRmServerManagementSession** Cmdlet은 Azure 서버 관리 세션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="8a56b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8a56b-109">EXAMPLES</span></span>

## <span data-ttu-id="8a56b-110">변수</span><span class="sxs-lookup"><span data-stu-id="8a56b-110">PARAMETERS</span></span>

### <span data-ttu-id="8a56b-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="8a56b-111">-Credential</span></span>
<span data-ttu-id="8a56b-112">서버 관리 세션에 대 한 연결에 대 한 **PSCredential** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="8a56b-113">자격 증명 개체를 가져오려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="8a56b-114">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="8a56b-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a56b-115">-노드</span><span class="sxs-lookup"><span data-stu-id="8a56b-115">-Node</span></span>
<span data-ttu-id="8a56b-116">이 cmdlet이 세션을 만드는 데 사용할 노드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-116">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="8a56b-117">이 매개 변수는 *ResourceGroupName* 및 *NodeName* 매개 변수 대신 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-117">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

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

### <span data-ttu-id="8a56b-118">-NodeName</span><span class="sxs-lookup"><span data-stu-id="8a56b-118">-NodeName</span></span>
<span data-ttu-id="8a56b-119">이 cmdlet이 세션을 만드는 노드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-119">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a56b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a56b-120">-ResourceGroupName</span></span>
<span data-ttu-id="8a56b-121">이 cmdlet이 세션을 만드는 노드의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-121">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

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

### <span data-ttu-id="8a56b-122">-세션 이름</span><span class="sxs-lookup"><span data-stu-id="8a56b-122">-SessionName</span></span>
<span data-ttu-id="8a56b-123">세션에 사용할 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-123">Specifies the name to use for the session.</span></span>

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

### <span data-ttu-id="8a56b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a56b-124">-DefaultProfile</span></span>
<span data-ttu-id="8a56b-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a56b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a56b-126">CommonParameters</span></span>
<span data-ttu-id="8a56b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a56b-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a56b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a56b-129">입력</span><span class="sxs-lookup"><span data-stu-id="8a56b-129">INPUTS</span></span>

### <span data-ttu-id="8a56b-130">노드나</span><span class="sxs-lookup"><span data-stu-id="8a56b-130">Node</span></span>
<span data-ttu-id="8a56b-131">' Node ' 매개 변수는 파이프라인에서 ' Node ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a56b-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="8a56b-132">출력</span><span class="sxs-lookup"><span data-stu-id="8a56b-132">OUTPUTS</span></span>

### <span data-ttu-id="8a56b-133">Microsoft. ServerManagement. Model. 세션</span><span class="sxs-lookup"><span data-stu-id="8a56b-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="8a56b-134">상속자</span><span class="sxs-lookup"><span data-stu-id="8a56b-134">NOTES</span></span>

## <span data-ttu-id="8a56b-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a56b-135">RELATED LINKS</span></span>

