---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstanceremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md
ms.openlocfilehash: 2b4133942a3aa7c4e9339579465942ade96c5709
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181796"
---
# <span data-ttu-id="bfab5-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="bfab5-101">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>

## <span data-ttu-id="bfab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfab5-102">SYNOPSIS</span></span>
<span data-ttu-id="bfab5-103">클라우드 서비스의 역할 인스턴스에 대한 원격 데스크톱 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bfab5-103">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="bfab5-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfab5-104">SYNTAX</span></span>

```
Get-AzCloudServiceRoleInstanceRemoteDesktopFile -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> -OutFile <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="bfab5-105">설명</span><span class="sxs-lookup"><span data-stu-id="bfab5-105">DESCRIPTION</span></span>
<span data-ttu-id="bfab5-106">클라우드 서비스의 역할 인스턴스에 대한 원격 데스크톱 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bfab5-106">Gets a remote desktop file for a role instance in a cloud service.</span></span>

## <span data-ttu-id="bfab5-107">예제</span><span class="sxs-lookup"><span data-stu-id="bfab5-107">EXAMPLES</span></span>

### <span data-ttu-id="bfab5-108">예제 1: RDP 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="bfab5-108">Example 1: Get an RDP file</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstanceRemoteDesktopFile -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0" -OutFile "C:\temp\ContosoFrontEnd_IN_0.rdp"
```

<span data-ttu-id="bfab5-109">이 명령은 ContosOrg라는 리소스 그룹에 속하는 \_ ContosoCS라는 클라우드 서비스의 0에서 ContosoFrontEnd라는 역할 인스턴스에 대한 \_ RDP 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bfab5-109">This command gets an RDP file for the role instance named ContosoFrontEnd\_IN\_0 of cloud Service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="bfab5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfab5-110">PARAMETERS</span></span>

### <span data-ttu-id="bfab5-111">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="bfab5-111">-CloudServiceName</span></span>
<span data-ttu-id="bfab5-112">.</span><span class="sxs-lookup"><span data-stu-id="bfab5-112">.</span></span>

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

### <span data-ttu-id="bfab5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfab5-113">-DefaultProfile</span></span>
<span data-ttu-id="bfab5-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfab5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfab5-115">-OutFile</span><span class="sxs-lookup"><span data-stu-id="bfab5-115">-OutFile</span></span>
<span data-ttu-id="bfab5-116">출력 파일을 쓸 경로</span><span class="sxs-lookup"><span data-stu-id="bfab5-116">Path to write output file to</span></span>

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

### <span data-ttu-id="bfab5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfab5-117">-PassThru</span></span>
<span data-ttu-id="bfab5-118">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bfab5-118">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfab5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfab5-119">-ResourceGroupName</span></span>
<span data-ttu-id="bfab5-120">.</span><span class="sxs-lookup"><span data-stu-id="bfab5-120">.</span></span>

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

### <span data-ttu-id="bfab5-121">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="bfab5-121">-RoleInstanceName</span></span>
<span data-ttu-id="bfab5-122">역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfab5-122">Name of the role instance.</span></span>

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

### <span data-ttu-id="bfab5-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bfab5-123">-SubscriptionId</span></span>
<span data-ttu-id="bfab5-124">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="bfab5-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bfab5-125">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="bfab5-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfab5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfab5-126">CommonParameters</span></span>
<span data-ttu-id="bfab5-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfab5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfab5-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfab5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfab5-129">입력</span><span class="sxs-lookup"><span data-stu-id="bfab5-129">INPUTS</span></span>

## <span data-ttu-id="bfab5-130">출력</span><span class="sxs-lookup"><span data-stu-id="bfab5-130">OUTPUTS</span></span>

### <span data-ttu-id="bfab5-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bfab5-131">System.Boolean</span></span>

## <span data-ttu-id="bfab5-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfab5-132">NOTES</span></span>

<span data-ttu-id="bfab5-133">별칭</span><span class="sxs-lookup"><span data-stu-id="bfab5-133">ALIASES</span></span>

## <span data-ttu-id="bfab5-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfab5-134">RELATED LINKS</span></span>

