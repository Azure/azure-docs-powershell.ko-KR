---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325730"
---
# <span data-ttu-id="e3d16-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3d16-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="e3d16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3d16-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d16-103">Azure Analysis Services 서버 cmdlet 요청에 사용할 인증된 계정을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="e3d16-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3d16-104">SYNTAX</span></span>

### <span data-ttu-id="e3d16-105">UserParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e3d16-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d16-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e3d16-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d16-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e3d16-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3d16-108">설명</span><span class="sxs-lookup"><span data-stu-id="e3d16-108">DESCRIPTION</span></span>
<span data-ttu-id="e3d16-109">Add-AzAnalysisServicesAccount cmdlet은 Azure Analysis Services 서버의 인스턴스에 로그인하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="e3d16-110">예제</span><span class="sxs-lookup"><span data-stu-id="e3d16-110">EXAMPLES</span></span>

### <span data-ttu-id="e3d16-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3d16-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="e3d16-112">이 예제에서는 $UserCredential 변수에 지정된 계정을 westcentralus.asazure.windows.net Analysis Services 환경에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="e3d16-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e3d16-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="e3d16-114">첫 번째 명령은 애플리케이션 서비스 주체 자격 증명을 인용한 다음, 애플리케이션 서비스 주체 자격 증명을 $ApplicationCredential 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="e3d16-115">두 번째 명령은 $ApplicationCredential 변수로 지정된 애플리케이션 서비스 주체 계정을 westcentralus.asazure.windows.net Analysis Services 환경에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="e3d16-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="e3d16-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="e3d16-117">이 예제에서는 ApplicationId, TenantId 및 CertificateThumbprint에서 지정한 애플리케이션 서비스 주체 계정을 westcentralus.asazure.windows.net Analysis Services 환경에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="e3d16-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3d16-118">PARAMETERS</span></span>

### <span data-ttu-id="e3d16-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e3d16-119">-ApplicationId</span></span>
<span data-ttu-id="e3d16-120">애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-120">The application ID.</span></span>

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

### <span data-ttu-id="e3d16-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e3d16-121">-CertificateThumbprint</span></span>
<span data-ttu-id="e3d16-122">인증서 해시(지문)</span><span class="sxs-lookup"><span data-stu-id="e3d16-122">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="e3d16-123">-Credential</span><span class="sxs-lookup"><span data-stu-id="e3d16-123">-Credential</span></span>
<span data-ttu-id="e3d16-124">로그인 자격 증명</span><span class="sxs-lookup"><span data-stu-id="e3d16-124">Login credentials</span></span>

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

### <span data-ttu-id="e3d16-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="e3d16-125">-RolloutEnvironment</span></span>
<span data-ttu-id="e3d16-126">로그온할 Azure Analysis Services 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="e3d16-127">서버의 전체 이름(예: asazure://westcentralus.asazure.windows.net/testserver)을 지정하면 이 변수에 대한 올바른 값이 westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="e3d16-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

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

### <span data-ttu-id="e3d16-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e3d16-128">-ServicePrincipal</span></span>
<span data-ttu-id="e3d16-129">서비스 주체 자격 증명을 제공하여 이 계정이 인증을 하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="e3d16-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e3d16-130">-TenantId</span></span>
<span data-ttu-id="e3d16-131">테넌트 이름 또는 ID</span><span class="sxs-lookup"><span data-stu-id="e3d16-131">Tenant name or ID</span></span>

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

### <span data-ttu-id="e3d16-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3d16-132">-Confirm</span></span>
<span data-ttu-id="e3d16-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3d16-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d16-134">-WhatIf</span></span>
<span data-ttu-id="e3d16-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e3d16-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3d16-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3d16-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d16-137">CommonParameters</span></span>
<span data-ttu-id="e3d16-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3d16-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d16-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e3d16-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d16-140">입력</span><span class="sxs-lookup"><span data-stu-id="e3d16-140">INPUTS</span></span>

### <span data-ttu-id="e3d16-141">없음</span><span class="sxs-lookup"><span data-stu-id="e3d16-141">None</span></span>

## <span data-ttu-id="e3d16-142">출력</span><span class="sxs-lookup"><span data-stu-id="e3d16-142">OUTPUTS</span></span>

### <span data-ttu-id="e3d16-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e3d16-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="e3d16-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3d16-144">NOTES</span></span>
<span data-ttu-id="e3d16-145">별칭: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="e3d16-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="e3d16-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3d16-146">RELATED LINKS</span></span>
