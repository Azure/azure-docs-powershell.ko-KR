---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: c447d8dbfb7ed0b1fb4cf2ac3ad4c63aa4666ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711565"
---
# <span data-ttu-id="4ad46-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4ad46-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="4ad46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ad46-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad46-103">클러스터에 대 한 HTTP 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad46-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ad46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ad46-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ad46-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4ad46-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad46-106">**AzureRmHDInsightHttpServicesAccess** CMDLET은 ODBC, Ambari, Oozie 및 웹 서비스를 사용 하 여 Azure HDInsight 클러스터에 대 한 HTTP 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad46-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="4ad46-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4ad46-107">EXAMPLES</span></span>

### <span data-ttu-id="4ad46-108">예제 1: Azure HDInsight 클러스터에 대 한 HTTP 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="4ad46-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="4ad46-109">이 명령은-hadoop-001 이라는 클러스터에 대 한 HTTP 액세스를 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad46-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4ad46-110">변수</span><span class="sxs-lookup"><span data-stu-id="4ad46-110">PARAMETERS</span></span>

### <span data-ttu-id="4ad46-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4ad46-111">-ClusterName</span></span>
<span data-ttu-id="4ad46-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad46-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad46-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4ad46-113">-HttpCredential</span></span>
<span data-ttu-id="4ad46-114">클러스터에 대 한 HTTP (클러스터 로그인) 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad46-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad46-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad46-115">-ResourceGroupName</span></span>
<span data-ttu-id="4ad46-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad46-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ad46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad46-117">-DefaultProfile</span></span>
<span data-ttu-id="4ad46-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad46-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ad46-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad46-119">CommonParameters</span></span>
<span data-ttu-id="4ad46-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad46-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad46-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ad46-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad46-122">입력</span><span class="sxs-lookup"><span data-stu-id="4ad46-122">INPUTS</span></span>

## <span data-ttu-id="4ad46-123">출력</span><span class="sxs-lookup"><span data-stu-id="4ad46-123">OUTPUTS</span></span>

### <span data-ttu-id="4ad46-124">HttpConnectivitySettings를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="4ad46-124">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="4ad46-125">상속자</span><span class="sxs-lookup"><span data-stu-id="4ad46-125">NOTES</span></span>

## <span data-ttu-id="4ad46-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ad46-126">RELATED LINKS</span></span>

[<span data-ttu-id="4ad46-127">철회-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4ad46-127">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


