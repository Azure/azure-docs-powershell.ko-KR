---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: 712e3a6f90e37a38584ba27ab1ef07da019dc06a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868318"
---
# <span data-ttu-id="e9a0e-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="e9a0e-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="e9a0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a0e-103">클러스터 구성 개체에 보안 프로필을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-103">Adds a security profileto a cluster configuration object.</span></span>

## <span data-ttu-id="e9a0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9a0e-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9a0e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e9a0e-105">DESCRIPTION</span></span>
<span data-ttu-id="e9a0e-106">보안 프로필을 kerberizing 하 여 보안 클러스터를 만드는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="e9a0e-107">보안 프로필 클러스터를 Active Directory 도메인에 참가 하는 것과 관련 된 구성을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="e9a0e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e9a0e-108">EXAMPLES</span></span>

### <span data-ttu-id="e9a0e-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9a0e-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e9a0e-110">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="e9a0e-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="e9a0e-111">변수</span><span class="sxs-lookup"><span data-stu-id="e9a0e-111">PARAMETERS</span></span>

### <span data-ttu-id="e9a0e-112">-Cluster사람들 Groupdns</span><span class="sxs-lookup"><span data-stu-id="e9a0e-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="e9a0e-113">Ambari 및 레인저에서 사용할 수 있는 Active Directory 그룹의 고유 이름</span><span class="sxs-lookup"><span data-stu-id="e9a0e-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="e9a0e-114">-구성</span><span class="sxs-lookup"><span data-stu-id="e9a0e-114">-Config</span></span>
<span data-ttu-id="e9a0e-115">이 cmdlet이 수정 하는 HDInsight 클러스터 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="e9a0e-116">이 개체는 New-AzHDInsightClusterConfig cmdlet에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="e9a0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a0e-117">-DefaultProfile</span></span>
<span data-ttu-id="e9a0e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e9a0e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9a0e-119">-도메인</span><span class="sxs-lookup"><span data-stu-id="e9a0e-119">-Domain</span></span>
<span data-ttu-id="e9a0e-120">클러스터의 Active Directory 도메인</span><span class="sxs-lookup"><span data-stu-id="e9a0e-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="e9a0e-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="e9a0e-121">-DomainUserCredential</span></span>
<span data-ttu-id="e9a0e-122">클러스터를 만들 수 있는 충분 한 권한이 있는 도메인 사용자 계정 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="e9a0e-123">사용자 이름은 형식 이어야 합니다. user@domain</span><span class="sxs-lookup"><span data-stu-id="e9a0e-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="e9a0e-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="e9a0e-124">-LdapsUrls</span></span>
<span data-ttu-id="e9a0e-125">Active Directory에 대 한 하나 또는 여러 개의 LDAPS 서버 url</span><span class="sxs-lookup"><span data-stu-id="e9a0e-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="e9a0e-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="e9a0e-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="e9a0e-127">Active directory에서 사용자 및 컴퓨터 계정이 생성 될 조직 구성 단위의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="e9a0e-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e9a0e-128">-Confirm</span></span>
<span data-ttu-id="e9a0e-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a0e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a0e-130">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a0e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a0e-131">CommonParameters</span></span>
<span data-ttu-id="e9a0e-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a0e-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9a0e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a0e-134">입력</span><span class="sxs-lookup"><span data-stu-id="e9a0e-134">INPUTS</span></span>

### <span data-ttu-id="e9a0e-135">AzureHDInsightConfig의. m m.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e9a0e-136">출력</span><span class="sxs-lookup"><span data-stu-id="e9a0e-136">OUTPUTS</span></span>

### <span data-ttu-id="e9a0e-137">AzureHDInsightSecurityProfile의. m m.</span><span class="sxs-lookup"><span data-stu-id="e9a0e-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="e9a0e-138">상속자</span><span class="sxs-lookup"><span data-stu-id="e9a0e-138">NOTES</span></span>

## <span data-ttu-id="e9a0e-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9a0e-139">RELATED LINKS</span></span>
