---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 09b389763897f91a23f56f0a3383dd3f7f03ca1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702372"
---
# <span data-ttu-id="71cb3-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71cb3-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="71cb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="71cb3-103">Windows 클러스터에 RDP 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71cb3-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71cb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71cb3-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71cb3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="71cb3-105">DESCRIPTION</span></span>
<span data-ttu-id="71cb3-106">**AzureRmHDInsightRdpServicesAccess** CMDLET은 RDP (원격 데스크톱 프로토콜)에서 Windows 기반 Azure HDInsight 클러스터에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="71cb3-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="71cb3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="71cb3-107">EXAMPLES</span></span>

### <span data-ttu-id="71cb3-108">예제 1: Azure HDInsight 클러스터에 RDP 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="71cb3-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="71cb3-109">이 명령은-hadoop-001 이라는 클러스터에 RDP 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71cb3-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="71cb3-110">변수</span><span class="sxs-lookup"><span data-stu-id="71cb3-110">PARAMETERS</span></span>

### <span data-ttu-id="71cb3-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="71cb3-111">-ClusterName</span></span>
<span data-ttu-id="71cb3-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71cb3-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="71cb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cb3-113">-DefaultProfile</span></span>
<span data-ttu-id="71cb3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="71cb3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71cb3-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="71cb3-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="71cb3-116">RDP가 클러스터에 액세스 하는 데 사용할 만료 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71cb3-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cb3-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="71cb3-117">-RdpCredential</span></span>
<span data-ttu-id="71cb3-118">클러스터의 RDP 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71cb3-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="71cb3-119">이는 Windows 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71cb3-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="71cb3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71cb3-120">-ResourceGroupName</span></span>
<span data-ttu-id="71cb3-121">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71cb3-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="71cb3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cb3-122">CommonParameters</span></span>
<span data-ttu-id="71cb3-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71cb3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cb3-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71cb3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cb3-125">입력</span><span class="sxs-lookup"><span data-stu-id="71cb3-125">INPUTS</span></span>

### <span data-ttu-id="71cb3-126">않아야</span><span class="sxs-lookup"><span data-stu-id="71cb3-126">None</span></span>
<span data-ttu-id="71cb3-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71cb3-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71cb3-128">출력</span><span class="sxs-lookup"><span data-stu-id="71cb3-128">OUTPUTS</span></span>

### <span data-ttu-id="71cb3-129">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="71cb3-129">System.Void</span></span>

## <span data-ttu-id="71cb3-130">상속자</span><span class="sxs-lookup"><span data-stu-id="71cb3-130">NOTES</span></span>

## <span data-ttu-id="71cb3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71cb3-131">RELATED LINKS</span></span>

[<span data-ttu-id="71cb3-132">철회-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71cb3-132">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


