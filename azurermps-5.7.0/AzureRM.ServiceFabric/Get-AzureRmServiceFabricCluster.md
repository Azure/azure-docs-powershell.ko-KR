---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/get-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5f034253326f551c5b1930f6cf90a80c83ed82f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526591"
---
# <span data-ttu-id="f2c1c-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f2c1c-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="f2c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c1c-103">클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2c1c-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2c1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2c1c-104">SYNTAX</span></span>

### <span data-ttu-id="f2c1c-105">BySubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="f2c1c-105">BySubscription (Default)</span></span>
```
Get-AzureRmServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2c1c-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f2c1c-106">ByResourceGroup</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2c1c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="f2c1c-107">ByName</span></span>
```
Get-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2c1c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f2c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="f2c1c-109">**추가-AzureRmServiceFabricCluster** 는 클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2c1c-109">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="f2c1c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f2c1c-110">EXAMPLES</span></span>

### <span data-ttu-id="f2c1c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2c1c-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="f2c1c-112">이 명령은 ' myCluster ' 클러스터에 대 한 클러스터 리소스 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2c1c-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="f2c1c-113">변수</span><span class="sxs-lookup"><span data-stu-id="f2c1c-113">PARAMETERS</span></span>

### <span data-ttu-id="f2c1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c1c-114">-DefaultProfile</span></span>
<span data-ttu-id="f2c1c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2c1c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2c1c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="f2c1c-116">-Name</span></span>
<span data-ttu-id="f2c1c-117">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2c1c-117">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c1c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2c1c-118">-ResourceGroupName</span></span>
<span data-ttu-id="f2c1c-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2c1c-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c1c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c1c-120">CommonParameters</span></span>
<span data-ttu-id="f2c1c-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2c1c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c1c-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2c1c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c1c-123">입력</span><span class="sxs-lookup"><span data-stu-id="f2c1c-123">INPUTS</span></span>

### <span data-ttu-id="f2c1c-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2c1c-124">System.String</span></span>

## <span data-ttu-id="f2c1c-125">출력</span><span class="sxs-lookup"><span data-stu-id="f2c1c-125">OUTPUTS</span></span>

### <span data-ttu-id="f2c1c-126">System.webserver. IList ' 1 [[ServiceFabric]. PsCluster, ServiceFabric, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]])]</span><span class="sxs-lookup"><span data-stu-id="f2c1c-126">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f2c1c-127">상속자</span><span class="sxs-lookup"><span data-stu-id="f2c1c-127">NOTES</span></span>

## <span data-ttu-id="f2c1c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2c1c-128">RELATED LINKS</span></span>

