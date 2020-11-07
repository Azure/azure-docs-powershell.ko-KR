---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: ddc269d342a6119187ec578e236a30c928d9ea3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868213"
---
# <span data-ttu-id="2123f-101">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2123f-101">Revoke-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="2123f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2123f-102">SYNOPSIS</span></span>
<span data-ttu-id="2123f-103">클러스터에 대 한 HTTP 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2123f-103">Disables HTTP access to the cluster.</span></span>

## <span data-ttu-id="2123f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2123f-104">SYNTAX</span></span>

```
Revoke-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2123f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2123f-105">DESCRIPTION</span></span>
<span data-ttu-id="2123f-106">**AzHDInsightHttpServicesAccess** CMDLET은 ODBC, Ambari, Oozie 및 webHCatalog 웹 서비스에 대 한 Azure HDInsight 클러스터에 대 한 HTTP 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2123f-106">The **Revoke-AzHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="2123f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2123f-107">EXAMPLES</span></span>

### <span data-ttu-id="2123f-108">예제 1: 클러스터에 대 한 HTTP 액세스 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="2123f-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="2123f-109">이 명령은 hadoop_001 인 클러스터에 대 한 HTTP 액세스를 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2123f-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="2123f-110">변수</span><span class="sxs-lookup"><span data-stu-id="2123f-110">PARAMETERS</span></span>

### <span data-ttu-id="2123f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2123f-111">-ClusterName</span></span>
<span data-ttu-id="2123f-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2123f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2123f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2123f-113">-DefaultProfile</span></span>
<span data-ttu-id="2123f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2123f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2123f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2123f-115">-ResourceGroupName</span></span>
<span data-ttu-id="2123f-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2123f-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2123f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2123f-117">CommonParameters</span></span>
<span data-ttu-id="2123f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2123f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2123f-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2123f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2123f-120">입력</span><span class="sxs-lookup"><span data-stu-id="2123f-120">INPUTS</span></span>

### <span data-ttu-id="2123f-121">않아야</span><span class="sxs-lookup"><span data-stu-id="2123f-121">None</span></span>

## <span data-ttu-id="2123f-122">출력</span><span class="sxs-lookup"><span data-stu-id="2123f-122">OUTPUTS</span></span>

### <span data-ttu-id="2123f-123">HttpConnectivitySettings를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="2123f-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="2123f-124">상속자</span><span class="sxs-lookup"><span data-stu-id="2123f-124">NOTES</span></span>

## <span data-ttu-id="2123f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2123f-125">RELATED LINKS</span></span>

[<span data-ttu-id="2123f-126">부여-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2123f-126">Grant-AzHDInsightHttpServicesAccess</span></span>](./Grant-AzHDInsightHttpServicesAccess.md)


