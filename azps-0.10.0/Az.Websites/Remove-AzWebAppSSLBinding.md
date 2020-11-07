---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: c2dc86d26dd6a35fc5830fc37b768ec7e14819a4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876121"
---
# <span data-ttu-id="b0e88-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b0e88-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="b0e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0e88-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e88-103">업로드 된 인증서에서 SSL 바인딩을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="b0e88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0e88-104">SYNTAX</span></span>

### <span data-ttu-id="b0e88-105">S1</span><span class="sxs-lookup"><span data-stu-id="b0e88-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0e88-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="b0e88-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0e88-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b0e88-107">DESCRIPTION</span></span>
<span data-ttu-id="b0e88-108">**AzWebAppSSLBinding** Cmdlet은 Azure 웹 앱에서 SSL (Secure Sockets layer) 바인딩을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="b0e88-109">SSL 바인딩은 웹 앱을 인증서와 연결 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="b0e88-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b0e88-110">EXAMPLES</span></span>

### <span data-ttu-id="b0e88-111">예제 1: 웹 앱에 대 한 SSL 바인딩 제거</span><span class="sxs-lookup"><span data-stu-id="b0e88-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="b0e88-112">이 명령은 웹 앱 ContosoWebApp에 대 한 SSL 바인딩을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="b0e88-113">*DeleteCertificate* 매개 변수가 포함 되지 않기 때문에 더 이상 SSL 바인딩이 없는 경우 인증서가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="b0e88-114">예제 2: 인증서를 제거 하지 않고 SSL 바인딩 제거</span><span class="sxs-lookup"><span data-stu-id="b0e88-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="b0e88-115">예제 1과 유사 하 게,이 명령은 웹 앱 ContosoWebApp SSL 바인딩도 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="b0e88-116">그러나이 경우 *DeleteCertificate* 매개 변수가 포함 되며 매개 변수 값이 $False 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="b0e88-117">이는 SSL 바인딩이 있는지 여부에 관계 없이 인증서가 삭제 되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="b0e88-118">예제 3: 개체 참조를 사용 하 여 SSL 바인딩 제거</span><span class="sxs-lookup"><span data-stu-id="b0e88-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="b0e88-119">이 예제에서는 웹 앱 웹 사이트에 대 한 개체 참조를 사용 하 여 웹 앱에 대 한 SSL 바인딩을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>

<span data-ttu-id="b0e88-120">첫 번째 명령은 Get-AzWebApp cmdlet을 사용 하 여 ContosoWebApp 이라는 웹 앱에 대 한 개체 참조를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="b0e88-121">해당 개체 참조는 $WebApp 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-121">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="b0e88-122">두 번째 명령은 개체 참조와 **remove-AzWebAppSSLBinding** cmdlet을 사용 하 여 SSL 바인딩을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="b0e88-123">변수</span><span class="sxs-lookup"><span data-stu-id="b0e88-123">PARAMETERS</span></span>

### <span data-ttu-id="b0e88-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e88-124">-DefaultProfile</span></span>
<span data-ttu-id="b0e88-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e88-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e88-126">-DeleteCertificate</span></span>
<span data-ttu-id="b0e88-127">제거할 SSL 바인딩이 인증서에 사용 되는 유일한 바인딩만 하는 경우 수행할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="b0e88-128">*DeleteCertificate* 가 $False으로 설정 되 면 바인딩이 삭제 될 때 인증서가 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="b0e88-129">*DeleteCertificate* 가 $True으로 설정 되거나 명령에 포함 되어 있지 않으면 SSL 바인딩과 함께 인증서가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>

<span data-ttu-id="b0e88-130">제거 하려는 SSL 바인딩이 인증서에 사용 되는 유일한 바인딩만 있는 경우에만 인증서가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="b0e88-131">인증서에 둘 이상의 바인딩이 있는 경우 *DeleteCertificate* 매개 변수의 값에 관계 없이 인증서가 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e88-132">-Force</span><span class="sxs-lookup"><span data-stu-id="b0e88-132">-Force</span></span>
<span data-ttu-id="b0e88-133">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e88-134">-이름</span><span class="sxs-lookup"><span data-stu-id="b0e88-134">-Name</span></span>
<span data-ttu-id="b0e88-135">웹 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-135">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e88-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e88-136">-ResourceGroupName</span></span>
<span data-ttu-id="b0e88-137">인증서가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="b0e88-138">동일한 명령에서 *ResourceGroupName* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e88-139">-슬롯</span><span class="sxs-lookup"><span data-stu-id="b0e88-139">-Slot</span></span>
<span data-ttu-id="b0e88-140">웹 앱 배포 슬롯을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="b0e88-141">배포 슬롯을 얻으려면 Get-AzWebAppSlot cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e88-142">-Web app</span><span class="sxs-lookup"><span data-stu-id="b0e88-142">-WebApp</span></span>
<span data-ttu-id="b0e88-143">웹 앱을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-143">Specifies a Web App.</span></span>
<span data-ttu-id="b0e88-144">웹 앱을 가져오려면 Get-AzWebApp cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

<span data-ttu-id="b0e88-145">*ResourceGroupName* 매개 변수 및/또는 *webappname* 과 동일한 명령에서 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0e88-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="b0e88-146">-WebAppName</span></span>
<span data-ttu-id="b0e88-147">웹 앱의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-147">Specifies the name of the Web App.</span></span>

<span data-ttu-id="b0e88-148">동일한 명령에서 *Webappname* 매개 변수와 *web app* 매개 변수를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e88-149">-확인</span><span class="sxs-lookup"><span data-stu-id="b0e88-149">-Confirm</span></span>
<span data-ttu-id="b0e88-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e88-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e88-151">-WhatIf</span></span>
<span data-ttu-id="b0e88-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e88-153">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e88-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0e88-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e88-155">CommonParameters</span></span>
<span data-ttu-id="b0e88-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e88-157">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e88-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e88-158">입력</span><span class="sxs-lookup"><span data-stu-id="b0e88-158">INPUTS</span></span>

### <span data-ttu-id="b0e88-159">Site</span><span class="sxs-lookup"><span data-stu-id="b0e88-159">Site</span></span>
<span data-ttu-id="b0e88-160">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0e88-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b0e88-161">출력</span><span class="sxs-lookup"><span data-stu-id="b0e88-161">OUTPUTS</span></span>

## <span data-ttu-id="b0e88-162">상속자</span><span class="sxs-lookup"><span data-stu-id="b0e88-162">NOTES</span></span>

## <span data-ttu-id="b0e88-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0e88-163">RELATED LINKS</span></span>

[<span data-ttu-id="b0e88-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b0e88-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="b0e88-165">새로운 AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b0e88-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="b0e88-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b0e88-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="b0e88-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b0e88-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


