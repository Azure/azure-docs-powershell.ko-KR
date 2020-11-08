---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: 1f841d8cb49463f1ca9ce9198fc6173bb7efe506
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212765"
---
# <span data-ttu-id="ada38-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="ada38-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="ada38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ada38-102">SYNOPSIS</span></span>
<span data-ttu-id="ada38-103">클러스터 구성 개체에 보안 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada38-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="ada38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ada38-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ada38-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ada38-105">DESCRIPTION</span></span>
<span data-ttu-id="ada38-106">보안 프로필을 kerberizing 하 여 보안 클러스터를 만드는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ada38-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="ada38-107">보안 프로필 클러스터를 Active Directory 도메인에 참가 하는 것과 관련 된 구성을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada38-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="ada38-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ada38-108">EXAMPLES</span></span>

### <span data-ttu-id="ada38-109">예제 1: 클러스터 구성 개체에 보안 프로필 추가</span><span class="sxs-lookup"><span data-stu-id="ada38-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="ada38-110">이 명령은-hadoop-001 이라는 보안 프로필 값을 클러스터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada38-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ada38-111">변수</span><span class="sxs-lookup"><span data-stu-id="ada38-111">PARAMETERS</span></span>

### <span data-ttu-id="ada38-112">-Cluster사람들 Groupdns</span><span class="sxs-lookup"><span data-stu-id="ada38-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="ada38-113">Ambari 및 레인저에서 사용할 수 있는 Active Directory 그룹의 고유 이름</span><span class="sxs-lookup"><span data-stu-id="ada38-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="ada38-114">-구성</span><span class="sxs-lookup"><span data-stu-id="ada38-114">-Config</span></span>
<span data-ttu-id="ada38-115">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada38-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ada38-116">이 개체는 New-AzHDInsightClusterConfig cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ada38-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="ada38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ada38-117">-DefaultProfile</span></span>
<span data-ttu-id="ada38-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ada38-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ada38-119">-도메인</span><span class="sxs-lookup"><span data-stu-id="ada38-119">-Domain</span></span>
<span data-ttu-id="ada38-120">클러스터의 Active Directory 도메인</span><span class="sxs-lookup"><span data-stu-id="ada38-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="ada38-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="ada38-121">-DomainUserCredential</span></span>
<span data-ttu-id="ada38-122">클러스터를 만들 수 있는 충분 한 권한이 있는 도메인 사용자 계정 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="ada38-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="ada38-123">사용자 이름은 형식 이어야 합니다. user@domain</span><span class="sxs-lookup"><span data-stu-id="ada38-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="ada38-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="ada38-124">-LdapsUrls</span></span>
<span data-ttu-id="ada38-125">Active Directory에 대 한 하나 또는 여러 개의 LDAPS 서버 url</span><span class="sxs-lookup"><span data-stu-id="ada38-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="ada38-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="ada38-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="ada38-127">Active directory에서 사용자 및 컴퓨터 계정이 생성 될 조직 구성 단위의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ada38-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="ada38-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ada38-128">-Confirm</span></span>
<span data-ttu-id="ada38-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada38-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ada38-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ada38-130">-WhatIf</span></span>
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

### <span data-ttu-id="ada38-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ada38-131">CommonParameters</span></span>
<span data-ttu-id="ada38-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ada38-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ada38-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ada38-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ada38-134">입력</span><span class="sxs-lookup"><span data-stu-id="ada38-134">INPUTS</span></span>

### <span data-ttu-id="ada38-135">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="ada38-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="ada38-136">출력</span><span class="sxs-lookup"><span data-stu-id="ada38-136">OUTPUTS</span></span>

### <span data-ttu-id="ada38-137">AzureHDInsightSecurityProfile의. m m.</span><span class="sxs-lookup"><span data-stu-id="ada38-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="ada38-138">상속자</span><span class="sxs-lookup"><span data-stu-id="ada38-138">NOTES</span></span>

## <span data-ttu-id="ada38-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ada38-139">RELATED LINKS</span></span>
