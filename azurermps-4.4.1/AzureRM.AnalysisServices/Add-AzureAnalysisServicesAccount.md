---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Add-AzureAnalysisServicesAccount.md
ms.openlocfilehash: 8b5133e62139fca02dc59f84e5fb714d2a35e675
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711790"
---
# <span data-ttu-id="ba1a3-101">Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ba1a3-101">Add-AzureAnalysisServicesAccount</span></span>

## <span data-ttu-id="ba1a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba1a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1a3-103">Azure Analysis Services server cmdlet 요청에 사용할 인증 된 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba1a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba1a3-104">SYNTAX</span></span>

### <span data-ttu-id="ba1a3-105">UserParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ba1a3-105">UserParameterSetName (Default)</span></span>
```
Add-AzureAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba1a3-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ba1a3-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential>
 [-ServicePrincipal] -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba1a3-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ba1a3-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzureAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba1a3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ba1a3-108">DESCRIPTION</span></span>
<span data-ttu-id="ba1a3-109">Add-AzureAnalysisServicesAccount cmdlet은 Azure Analysis Services 서버 인스턴스에 로그인 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-109">The Add-AzureAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="ba1a3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ba1a3-110">EXAMPLES</span></span>

### <span data-ttu-id="ba1a3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba1a3-111">Example 1</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="ba1a3-112">이 예제는 $UserCredential 변수에 의해 지정 된 계정을 westcentralus.asazure.windows.net Analysis Services 환경에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="ba1a3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="ba1a3-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="ba1a3-114">첫 번째 명령은 응용 프로그램 서비스 사용자 자격 증명을 가져온 다음 $ApplicationCredential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="ba1a3-115">두 번째 명령은 $ApplicationCredential 변수에 지정 된 응용 프로그램 서비스 계정 계정을 추가 하 고 TenantId를 westcentralus.asazure.windows.net Analysis Services 환경으로 다시 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="ba1a3-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="ba1a3-116">Example 3</span></span>
```
PS C:\>Add-AzureAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="ba1a3-117">이 예제에서는 ApplicationId, TenantId, CertificateThumbprint에 의해 지정 된 응용 프로그램 서비스 계정 계정을 westcentralus.asazure.windows.net Analysis Services 환경에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="ba1a3-118">변수</span><span class="sxs-lookup"><span data-stu-id="ba1a3-118">PARAMETERS</span></span>

### <span data-ttu-id="ba1a3-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ba1a3-119">-ApplicationId</span></span>
<span data-ttu-id="ba1a3-120">응용 프로그램 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1a3-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ba1a3-121">-CertificateThumbprint</span></span>
<span data-ttu-id="ba1a3-122">인증서 해시 (지문)</span><span class="sxs-lookup"><span data-stu-id="ba1a3-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1a3-123">-Credential</span><span class="sxs-lookup"><span data-stu-id="ba1a3-123">-Credential</span></span>
<span data-ttu-id="ba1a3-124">로그인 자격 증명</span><span class="sxs-lookup"><span data-stu-id="ba1a3-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1a3-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="ba1a3-125">-RolloutEnvironment</span></span>
<span data-ttu-id="ba1a3-126">로그온 할 Azure Analysis Services 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="ba1a3-127">서버에 대 한 전체 이름 (예: asazure://westcentralus.asazure.windows.net/testserver)이 지정 된 경우이 변수의 올바른 값이 westcentralus.asazure.windows.net 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1a3-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ba1a3-128">-ServicePrincipal</span></span>
<span data-ttu-id="ba1a3-129">이 계정이 서비스 사용자 자격 증명을 제공 하 여 인증 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1a3-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ba1a3-130">-TenantId</span></span>
<span data-ttu-id="ba1a3-131">테 넌 트 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="ba1a3-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1a3-132">-확인</span><span class="sxs-lookup"><span data-stu-id="ba1a3-132">-Confirm</span></span>
<span data-ttu-id="ba1a3-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba1a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba1a3-134">-WhatIf</span></span>
<span data-ttu-id="ba1a3-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba1a3-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba1a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1a3-137">CommonParameters</span></span>
<span data-ttu-id="ba1a3-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1a3-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba1a3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1a3-140">입력</span><span class="sxs-lookup"><span data-stu-id="ba1a3-140">INPUTS</span></span>

## <span data-ttu-id="ba1a3-141">출력</span><span class="sxs-lookup"><span data-stu-id="ba1a3-141">OUTPUTS</span></span>

### <span data-ttu-id="ba1a3-142">AnalysisServices 평면. AsAzureProfile.</span><span class="sxs-lookup"><span data-stu-id="ba1a3-142">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="ba1a3-143">상속자</span><span class="sxs-lookup"><span data-stu-id="ba1a3-143">NOTES</span></span>
<span data-ttu-id="ba1a3-144">별칭: Login-AzureAsAccount</span><span class="sxs-lookup"><span data-stu-id="ba1a3-144">Alias: Login-AzureAsAccount</span></span>

## <span data-ttu-id="ba1a3-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba1a3-145">RELATED LINKS</span></span>

