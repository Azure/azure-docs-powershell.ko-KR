---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 529eedf9cd8ae782d08af7d349d4e11885a8a564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528136"
---
# <span data-ttu-id="e2af9-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e2af9-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="e2af9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2af9-102">SYNOPSIS</span></span>
<span data-ttu-id="e2af9-103">클러스터에 대 한 HTTP 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2af9-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2af9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2af9-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2af9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2af9-105">DESCRIPTION</span></span>
<span data-ttu-id="e2af9-106">**AzureRmHDInsightHttpServicesAccess** CMDLET은 ODBC, Ambari, Oozie 및 웹 서비스를 사용 하 여 Azure HDInsight 클러스터에 대 한 HTTP 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2af9-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="e2af9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e2af9-107">EXAMPLES</span></span>

### <span data-ttu-id="e2af9-108">예제 1: Azure HDInsight 클러스터에 대 한 HTTP 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="e2af9-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="e2af9-109">이 명령은-hadoop-001 이라는 클러스터에 대 한 HTTP 액세스를 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2af9-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e2af9-110">변수</span><span class="sxs-lookup"><span data-stu-id="e2af9-110">PARAMETERS</span></span>

### <span data-ttu-id="e2af9-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e2af9-111">-ClusterName</span></span>
<span data-ttu-id="e2af9-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2af9-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e2af9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2af9-113">-DefaultProfile</span></span>
<span data-ttu-id="e2af9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e2af9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2af9-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e2af9-115">-HttpCredential</span></span>
<span data-ttu-id="e2af9-116">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2af9-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2af9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2af9-117">-ResourceGroupName</span></span>
<span data-ttu-id="e2af9-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2af9-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e2af9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2af9-119">CommonParameters</span></span>
<span data-ttu-id="e2af9-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2af9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2af9-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2af9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2af9-122">입력</span><span class="sxs-lookup"><span data-stu-id="e2af9-122">INPUTS</span></span>

### <span data-ttu-id="e2af9-123">않아야</span><span class="sxs-lookup"><span data-stu-id="e2af9-123">None</span></span>
<span data-ttu-id="e2af9-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2af9-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2af9-125">출력</span><span class="sxs-lookup"><span data-stu-id="e2af9-125">OUTPUTS</span></span>

### <span data-ttu-id="e2af9-126">HttpConnectivitySettings를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="e2af9-126">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="e2af9-127">상속자</span><span class="sxs-lookup"><span data-stu-id="e2af9-127">NOTES</span></span>

## <span data-ttu-id="e2af9-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2af9-128">RELATED LINKS</span></span>

[<span data-ttu-id="e2af9-129">철회-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e2af9-129">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


