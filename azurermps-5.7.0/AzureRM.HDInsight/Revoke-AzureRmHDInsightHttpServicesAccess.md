---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 388e339ba7545bc2e4d00166a6f365a19cb44f28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532162"
---
# <span data-ttu-id="a597e-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a597e-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="a597e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a597e-102">SYNOPSIS</span></span>
<span data-ttu-id="a597e-103">클러스터에 대 한 HTTP 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a597e-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a597e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a597e-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a597e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a597e-105">DESCRIPTION</span></span>
<span data-ttu-id="a597e-106">**AzureRmHDInsightHttpServicesAccess** CMDLET은 ODBC, Ambari, Oozie 및 webHCatalog 웹 서비스에 대 한 Azure HDInsight 클러스터에 대 한 HTTP 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a597e-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="a597e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a597e-107">EXAMPLES</span></span>

### <span data-ttu-id="a597e-108">예제 1: 클러스터에 대 한 HTTP 액세스 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a597e-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="a597e-109">이 명령은 hadoop_001 인 클러스터에 대 한 HTTP 액세스를 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a597e-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="a597e-110">변수</span><span class="sxs-lookup"><span data-stu-id="a597e-110">PARAMETERS</span></span>

### <span data-ttu-id="a597e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a597e-111">-ClusterName</span></span>
<span data-ttu-id="a597e-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a597e-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a597e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a597e-113">-DefaultProfile</span></span>
<span data-ttu-id="a597e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a597e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a597e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a597e-115">-ResourceGroupName</span></span>
<span data-ttu-id="a597e-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a597e-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a597e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a597e-117">CommonParameters</span></span>
<span data-ttu-id="a597e-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a597e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a597e-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a597e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a597e-120">입력</span><span class="sxs-lookup"><span data-stu-id="a597e-120">INPUTS</span></span>

### <span data-ttu-id="a597e-121">않아야</span><span class="sxs-lookup"><span data-stu-id="a597e-121">None</span></span>
<span data-ttu-id="a597e-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a597e-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a597e-123">출력</span><span class="sxs-lookup"><span data-stu-id="a597e-123">OUTPUTS</span></span>

### <span data-ttu-id="a597e-124">HttpConnectivitySettings를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="a597e-124">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="a597e-125">상속자</span><span class="sxs-lookup"><span data-stu-id="a597e-125">NOTES</span></span>

## <span data-ttu-id="a597e-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a597e-126">RELATED LINKS</span></span>

[<span data-ttu-id="a597e-127">부여-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a597e-127">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)


