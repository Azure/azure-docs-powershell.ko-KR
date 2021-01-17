---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491434"
---
# <span data-ttu-id="979a9-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="979a9-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="979a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="979a9-102">SYNOPSIS</span></span>
<span data-ttu-id="979a9-103">업로드된 인증서에서 SSL 바인딩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="979a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="979a9-104">SYNTAX</span></span>

### <span data-ttu-id="979a9-105">S1</span><span class="sxs-lookup"><span data-stu-id="979a9-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="979a9-106">S2</span><span class="sxs-lookup"><span data-stu-id="979a9-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="979a9-107">설명</span><span class="sxs-lookup"><span data-stu-id="979a9-107">DESCRIPTION</span></span>
<span data-ttu-id="979a9-108">**Remove-AzWebAppSSLBinding** cmdlet은 Azure 웹앱에서 Secure Sockets Layer(SSL) 바인딩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="979a9-109">SSL 바인딩은 웹앱을 인증서와 연결하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="979a9-110">예제</span><span class="sxs-lookup"><span data-stu-id="979a9-110">EXAMPLES</span></span>

### <span data-ttu-id="979a9-111">예제 1: 웹앱에 대한 SSL 바인딩 제거</span><span class="sxs-lookup"><span data-stu-id="979a9-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="979a9-112">이 명령은 웹앱 ContosoWebApp에 대한 SSL 바인딩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="979a9-113">*DeleteCertificate* 매개 변수가 포함되지 않은 경우 더 이상 SSL 바인딩이 없는 경우 인증서가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="979a9-114">예제 2: 인증서를 제거하지 않고 SSL 바인딩 제거</span><span class="sxs-lookup"><span data-stu-id="979a9-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="979a9-115">예제 1과 마찬가지로 이 명령은 웹앱 ContosoWebApp에 대한 SSL 바인딩도 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="979a9-116">그러나 이 경우 *DeleteCertificate* 매개 변수가 포함되고 매개 변수 값이 $False.</span><span class="sxs-lookup"><span data-stu-id="979a9-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="979a9-117">즉, SSL 바인딩이 있는지 여부에 관계없이 인증서가 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="979a9-118">예제 3: 개체 참조를 사용하여 SSL 바인딩 제거</span><span class="sxs-lookup"><span data-stu-id="979a9-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="979a9-119">이 예제에서는 웹앱 웹 사이트에 대한 개체 참조를 사용하여 웹앱에 대한 SSL 바인딩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="979a9-120">첫 번째 명령은 Get-AzWebApp cmdlet을 사용하여 ContosoWebApp이라는 웹앱에 대한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="979a9-121">해당 개체 참조는 $WebApp.</span><span class="sxs-lookup"><span data-stu-id="979a9-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="979a9-122">두 번째 명령은 개체 참조 및 **Remove-AzWebAppSSLBinding** cmdlet을 사용하여 SSL 바인딩을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="979a9-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="979a9-123">PARAMETERS</span></span>

### <span data-ttu-id="979a9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="979a9-124">-DefaultProfile</span></span>
<span data-ttu-id="979a9-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="979a9-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="979a9-126">-DeleteCertificate</span></span>
<span data-ttu-id="979a9-127">제거되는 SSL 바인딩이 인증서에서 사용되는 유일한 바인딩인 경우 수행되는 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="979a9-128">*DeleteCertificate를* $False 바인딩이 삭제될 때 인증서가 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="979a9-129">*DeleteCertificate를* $True 명령에 포함되지 않은 경우 인증서가 SSL 바인딩과 함께 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="979a9-130">제거되는 SSL 바인딩이 인증서에서 사용되는 유일한 바인딩인 경우 인증서가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="979a9-131">인증서에 두 개 이상의 바인딩이 있는 경우 *DeleteCertificate* 매개 변수의 값에 관계없이 인증서가 제거되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a9-132">-Force</span><span class="sxs-lookup"><span data-stu-id="979a9-132">-Force</span></span>
<span data-ttu-id="979a9-133">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a9-134">-Name</span><span class="sxs-lookup"><span data-stu-id="979a9-134">-Name</span></span>
<span data-ttu-id="979a9-135">웹앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="979a9-136">-ResourceGroupName</span></span>
<span data-ttu-id="979a9-137">인증서가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="979a9-138">동일한 명령에서 *ResourceGroupName* 매개 변수 및 *WebApp* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a9-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="979a9-139">-Slot</span></span>
<span data-ttu-id="979a9-140">웹앱 배포 슬롯을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="979a9-141">배포 슬롯을 얻습니다. Get-AzWebAppSlot cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a9-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="979a9-142">-WebApp</span></span>
<span data-ttu-id="979a9-143">웹앱을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-143">Specifies a Web App.</span></span>
<span data-ttu-id="979a9-144">웹앱을 얻습니다. Get-AzWebApp cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="979a9-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="979a9-145">*ResourceGroupName* 매개 변수 및/또는 *WebAppName과* 동일한 명령에서 *WebApp* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="979a9-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="979a9-146">-WebAppName</span></span>
<span data-ttu-id="979a9-147">웹앱의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="979a9-148">동일한 명령에서 *WebAppName* 매개 변수 및 *WebApp* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="979a9-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="979a9-149">-Confirm</span></span>
<span data-ttu-id="979a9-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="979a9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="979a9-151">-WhatIf</span></span>
<span data-ttu-id="979a9-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="979a9-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="979a9-153">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="979a9-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="979a9-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="979a9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="979a9-155">CommonParameters</span></span>
<span data-ttu-id="979a9-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="979a9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="979a9-157">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="979a9-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="979a9-158">입력</span><span class="sxs-lookup"><span data-stu-id="979a9-158">INPUTS</span></span>

### <span data-ttu-id="979a9-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="979a9-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="979a9-160">출력</span><span class="sxs-lookup"><span data-stu-id="979a9-160">OUTPUTS</span></span>

### <span data-ttu-id="979a9-161">System.Void</span><span class="sxs-lookup"><span data-stu-id="979a9-161">System.Void</span></span>

## <span data-ttu-id="979a9-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="979a9-162">NOTES</span></span>

## <span data-ttu-id="979a9-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="979a9-163">RELATED LINKS</span></span>

[<span data-ttu-id="979a9-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="979a9-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="979a9-165">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="979a9-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="979a9-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="979a9-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="979a9-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="979a9-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


