---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: 17d7f922f5af46aa99e3b01aa0c0f63df05effe7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529163"
---
# <span data-ttu-id="a622d-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="a622d-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="a622d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a622d-102">SYNOPSIS</span></span>
<span data-ttu-id="a622d-103">그룹 구성원을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a622d-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a622d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a622d-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a622d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a622d-105">DESCRIPTION</span></span>
<span data-ttu-id="a622d-106">그룹 구성원을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a622d-106">Get a group members.</span></span>

## <span data-ttu-id="a622d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a622d-107">EXAMPLES</span></span>

### <span data-ttu-id="a622d-108">그룹 개체 id를 사용 하 여 그룹 구성원을--------------------------필터링--------------------------</span><span class="sxs-lookup"><span data-stu-id="a622d-108">--------------------------  Filters group members using group object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="a622d-109">85F89C90-780E-4AA6-9F4F-6F268D322EEE id를 사용 하 여 그룹 구성원을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a622d-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="a622d-110">변수</span><span class="sxs-lookup"><span data-stu-id="a622d-110">PARAMETERS</span></span>

### <span data-ttu-id="a622d-111">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="a622d-111">-GroupObjectId</span></span>
<span data-ttu-id="a622d-112">그룹의 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a622d-112">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a622d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a622d-113">-DefaultProfile</span></span>
<span data-ttu-id="a622d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a622d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a622d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a622d-115">CommonParameters</span></span>
<span data-ttu-id="a622d-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a622d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a622d-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a622d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a622d-118">입력</span><span class="sxs-lookup"><span data-stu-id="a622d-118">INPUTS</span></span>

## <span data-ttu-id="a622d-119">출력</span><span class="sxs-lookup"><span data-stu-id="a622d-119">OUTPUTS</span></span>

### <span data-ttu-id="a622d-120">ActiveDirectory에서 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 목록 '을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a622d-120">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="a622d-121">상속자</span><span class="sxs-lookup"><span data-stu-id="a622d-121">NOTES</span></span>

## <span data-ttu-id="a622d-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a622d-122">RELATED LINKS</span></span>

[<span data-ttu-id="a622d-123">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="a622d-123">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="a622d-124">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a622d-124">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

