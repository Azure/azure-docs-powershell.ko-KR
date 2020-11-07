---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 6cbe18311f4a14b31bc50f7c0b95266bf99d4a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689823"
---
# <span data-ttu-id="ebbc7-101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ebbc7-101">Grant-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="ebbc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebbc7-102">SYNOPSIS</span></span>
<span data-ttu-id="ebbc7-103">Windows 클러스터에 RDP 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebbc7-103">Grants RDP access to the Windows cluster.</span></span>

## <span data-ttu-id="ebbc7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebbc7-104">SYNTAX</span></span>

```
Grant-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebbc7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ebbc7-105">DESCRIPTION</span></span>
<span data-ttu-id="ebbc7-106">**AzHDInsightRdpServicesAccess** CMDLET은 RDP (원격 데스크톱 프로토콜)에서 Windows 기반 Azure HDInsight 클러스터에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebbc7-106">The **Grant-AzHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ebbc7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ebbc7-107">EXAMPLES</span></span>

### <span data-ttu-id="ebbc7-108">예제 1: Azure HDInsight 클러스터에 RDP 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="ebbc7-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="ebbc7-109">이 명령은-hadoop-001 이라는 클러스터에 RDP 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebbc7-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ebbc7-110">변수</span><span class="sxs-lookup"><span data-stu-id="ebbc7-110">PARAMETERS</span></span>

### <span data-ttu-id="ebbc7-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ebbc7-111">-ClusterName</span></span>
<span data-ttu-id="ebbc7-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebbc7-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ebbc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebbc7-113">-DefaultProfile</span></span>
<span data-ttu-id="ebbc7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ebbc7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebbc7-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="ebbc7-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="ebbc7-116">RDP가 클러스터에 액세스 하는 데 사용할 만료 **날짜를 DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebbc7-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebbc7-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="ebbc7-117">-RdpCredential</span></span>
<span data-ttu-id="ebbc7-118">클러스터의 RDP 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebbc7-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="ebbc7-119">이는 Windows 클러스터에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebbc7-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="ebbc7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebbc7-120">-ResourceGroupName</span></span>
<span data-ttu-id="ebbc7-121">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebbc7-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ebbc7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebbc7-122">CommonParameters</span></span>
<span data-ttu-id="ebbc7-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebbc7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebbc7-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebbc7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebbc7-125">입력</span><span class="sxs-lookup"><span data-stu-id="ebbc7-125">INPUTS</span></span>

### <span data-ttu-id="ebbc7-126">않아야</span><span class="sxs-lookup"><span data-stu-id="ebbc7-126">None</span></span>

## <span data-ttu-id="ebbc7-127">출력</span><span class="sxs-lookup"><span data-stu-id="ebbc7-127">OUTPUTS</span></span>

### <span data-ttu-id="ebbc7-128">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ebbc7-128">System.Void</span></span>

## <span data-ttu-id="ebbc7-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ebbc7-129">NOTES</span></span>

## <span data-ttu-id="ebbc7-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebbc7-130">RELATED LINKS</span></span>

[<span data-ttu-id="ebbc7-131">철회-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ebbc7-131">Revoke-AzHDInsightRdpServicesAccess</span></span>](./Revoke-AzHDInsightRdpServicesAccess.md)


