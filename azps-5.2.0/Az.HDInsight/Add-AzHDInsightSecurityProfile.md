---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c44fea946f98c6ac19e77e7012910afac37bff7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340005"
---
# <span data-ttu-id="4c092-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="4c092-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="4c092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c092-102">SYNOPSIS</span></span>
<span data-ttu-id="4c092-103">클러스터 구성 개체에 보안 프로필을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="4c092-104">구문</span><span class="sxs-lookup"><span data-stu-id="4c092-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -DomainResourceId <String>
 -DomainUserCredential <PSCredential> [-OrganizationalUnitDN <String>] -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c092-105">설명</span><span class="sxs-lookup"><span data-stu-id="4c092-105">DESCRIPTION</span></span>
<span data-ttu-id="4c092-106">보안 프로필은 커버그하여 보안 클러스터를 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="4c092-107">보안 프로필에는 클러스터를 Active Directory 도메인에 조인하는 구성이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="4c092-108">예제</span><span class="sxs-lookup"><span data-stu-id="4c092-108">EXAMPLES</span></span>

### <span data-ttu-id="4c092-109">예제 1: 클러스터 구성 개체에 보안 프로필 추가</span><span class="sxs-lookup"><span data-stu-id="4c092-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

#Security profile info
PS C:\> $domain="sampledomain.onmicrosoft.com"
PS C:\> $domainUser="sample.user@sampledomain.onmicrosoft.com"
PS C:\> $domainPassword=ConvertTo-SecureString "domainPassword" -AsPlainText -Force
PS C:\> $domainUserCredential=New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
PS C:\> $organizationalUnitDN="ou=testunitdn"
PS C:\> $ldapsUrls=("ldaps://sampledomain.onmicrosoft.com:636","ldaps://sampledomain.onmicrosoft.com:389")
PS C:\> $clusterUsersGroupDNs=("groupdn1","groupdn2")

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightSecurityProfile `
                -Domain $domain `
                -DomainUserCredential $domainUserCredential `
                -OrganizationalUnitDN $organizationalUnitDN `
                -LdapsUrls $ldapsUrls `
                -ClusterUsersGroupDNs $clusterUsersGroupDNs `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="4c092-110">이 명령은 your-hadoop-001이라는 클러스터에 보안 프로필 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="4c092-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c092-111">PARAMETERS</span></span>

### <span data-ttu-id="4c092-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="4c092-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="4c092-113">Ambari 및 Ranger에서 사용할 수 있는 Active Directory 그룹의 고유 이름</span><span class="sxs-lookup"><span data-stu-id="4c092-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c092-114">-Config</span><span class="sxs-lookup"><span data-stu-id="4c092-114">-Config</span></span>
<span data-ttu-id="4c092-115">이 cmdlet이 수정하는 HDInsight 클러스터 구성 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="4c092-116">이 개체는 New-AzHDInsightClusterConfig cmdlet에 의해 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c092-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c092-117">-DefaultProfile</span></span>
<span data-ttu-id="4c092-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4c092-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c092-119">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="4c092-119">-DomainResourceId</span></span>
<span data-ttu-id="4c092-120">클러스터에 대한 Active Directory 도메인 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-120">Active Directory domain resource id for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c092-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="4c092-121">-DomainUserCredential</span></span>
<span data-ttu-id="4c092-122">클러스터를 만들기 위한 충분한 권한이 있는 도메인 사용자 계정 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="4c092-123">사용자 이름은 형식이 user@domain 지정되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-123">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c092-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="4c092-124">-LdapsUrls</span></span>
<span data-ttu-id="4c092-125">Active Directory에 대한 하나 또는 여러 LDAPS 서버의 URL</span><span class="sxs-lookup"><span data-stu-id="4c092-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c092-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="4c092-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="4c092-127">사용자 및 컴퓨터 계정을 만들 Active Directory에서 조직 구성 단위의 고유 이름</span><span class="sxs-lookup"><span data-stu-id="4c092-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="4c092-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c092-128">-Confirm</span></span>
<span data-ttu-id="4c092-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c092-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c092-130">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c092-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c092-131">CommonParameters</span></span>
<span data-ttu-id="4c092-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4c092-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c092-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c092-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c092-134">입력</span><span class="sxs-lookup"><span data-stu-id="4c092-134">INPUTS</span></span>

### <span data-ttu-id="4c092-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4c092-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="4c092-136">출력</span><span class="sxs-lookup"><span data-stu-id="4c092-136">OUTPUTS</span></span>

### <span data-ttu-id="4c092-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="4c092-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="4c092-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4c092-138">NOTES</span></span>

## <span data-ttu-id="4c092-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c092-139">RELATED LINKS</span></span>
